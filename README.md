# Image Caption Generator using CNN-LSTM

## Project Overview
This project implements an Image Caption Generator using a **Convolutional Neural Network (CNN)** and **Long Short-Term Memory (LSTM)** from scratch. The model takes an image as input and generates a meaningful caption describing the content of the image.

## Objectives
- Develop an image caption generator model using CNN and LSTM.
- Train the model from scratch and optimize it using **hyperparameter tuning** and **cross-validation**.
- Evaluate the model using standard captioning metrics such as **BLEU**, **ROUGE**, and **METEOR**.

## Dataset
The dataset used in this project consists of 8,091 images, each annotated with five different captions, providing clear descriptions of key entities and events. The dataset can be accessed through the project link (make sure to mention how to download the dataset or provide access).

## Model Architecture
The model consists of two primary components:
1. **CNN (InceptionV3)**: A pre-trained CNN model is used for feature extraction from the images. The last convolutional layer outputs a feature vector representing the image.
2. **LSTM**: The extracted image features are fed into an LSTM network, which generates a sequence of words (caption) one word at a time.

The architecture is designed as follows:
- **Input Layer (CNN Features)**: Extracts features from images using InceptionV3.
- **Embedding Layer**: Converts each word of the caption into an embedding.
- **LSTM Layer**: Generates captions based on image features.
- **Dense Layer**: Produces the final output, which is the next word in the caption.

## Steps Involved

### 1. **Data Preprocessing**:
- **Images**: Resizing, normalizing, and converting them into feature vectors using InceptionV3.
- **Captions**: Tokenization, padding, and conversion to integer sequences.

### 2. **Model Development**:
- The **CNN-LSTM architecture** is implemented, where CNN extracts features and LSTM generates captions.

### 3. **Training**:
- The model is trained using the image-caption pairs, optimizing for the next word prediction using **categorical cross-entropy** loss.

### 4. **Evaluation**:
- The model is evaluated using metrics such as **BLEU score**, **ROUGE**, and **METEOR**.

## Installation

To run the project locally, clone this repository and install the necessary dependencies:

```bash
git clone https://github.com/UdaraChamidu/image-caption-generator.git
cd image-caption-generator
pip install -r requirements.txt
