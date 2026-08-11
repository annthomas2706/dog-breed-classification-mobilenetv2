# Dog Breed Classification using MobileNetV2

A deep learning project for classifying images into different dog breeds using transfer learning with a pretrained MobileNetV2 model.

## Overview

This project uses TensorFlow and Keras to build a dog breed image classification model. A pretrained MobileNetV2 model with ImageNet weights is used as the base model, followed by Global Average Pooling and a Dense classification layer.

The project covers the complete deep learning workflow, including:

- Image preprocessing
- Creating TensorFlow data pipelines
- Batching and preparing image datasets
- Transfer learning with MobileNetV2
- Model training and validation
- Early stopping
- Model evaluation
- Generating predictions
- Visualizing predictions

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Model Architecture

The model uses:

1. Pretrained MobileNetV2
2. GlobalAveragePooling2D
3. Dense output layer with Softmax activation

```text
Input Image
     ↓
MobileNetV2
     ↓
GlobalAveragePooling2D
     ↓
Dense Layer
     ↓
Softmax
     ↓
Predicted Dog Breed

---


