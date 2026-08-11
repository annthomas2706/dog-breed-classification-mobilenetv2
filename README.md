# Dog Breed Classification using MobileNetV2

A deep learning project for classifying images into different dog breeds using Transfer Learning with a pretrained MobileNetV2 model.

## Overview

This project uses TensorFlow and Keras to build a multi-class dog breed image classification model.

A pretrained MobileNetV2 model with ImageNet weights is used as the base model, followed by Global Average Pooling and a Dense classification layer.

The project covers the complete deep learning workflow, from dataset preparation and image preprocessing to model training, evaluation, prediction, and visualization.

## Dataset

This project uses the **Dog Breed Identification dataset** from Kaggle's Dog Breed Identification competition.

The dataset contains images of different dog breeds along with their corresponding breed labels.

Dataset:  
https://www.kaggle.com/c/dog-breed-identification/data

The dataset is not included in this repository because of its large size.

### Dataset Setup

1. Download the dataset from Kaggle.
2. Extract the downloaded files.
3. Place the dataset in your working directory or Google Drive.
4. Update the dataset path in the notebook.
5. Run the notebook.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Google Colab

## Project Workflow

The project follows these steps:

1. Load the dataset
2. Explore the dog breed data
3. Prepare image paths and labels
4. Split the data into training and validation sets
5. Load and decode images
6. Convert images to RGB
7. Resize images to 224 × 224 pixels
8. Apply MobileNetV2 preprocessing
9. Create TensorFlow data pipelines
10. Batch and prefetch the datasets
11. Apply transfer learning using MobileNetV2
12. Add Global Average Pooling
13. Add a Dense classification layer with Softmax activation
14. Train the model
15. Apply Early Stopping
16. Evaluate the model
17. Generate predictions
18. Visualize predictions

## Model Architecture

The model uses:

- Pretrained MobileNetV2
- GlobalAveragePooling2D
- Dense classification layer
- Softmax activation

The original ImageNet classification layer is removed so that MobileNetV2 can be adapted to classify the dog breeds in this dataset.

### Model Flow

Input Image → MobileNetV2 → Global Average Pooling → Dense Layer → Softmax → Predicted Dog Breed

## Transfer Learning

Transfer learning is used to take advantage of features already learned by MobileNetV2 from the ImageNet dataset.

Instead of training a CNN completely from scratch, the pretrained model is adapted for the dog breed classification task.

This helps reduce training time and allows the model to make use of previously learned visual features.

## Image Preprocessing

The images go through the following preprocessing steps:

- Image loading
- JPEG decoding
- RGB conversion
- Resizing to 224 × 224 pixels
- MobileNetV2 preprocessing
- TensorFlow dataset creation
- Batching
- Prefetching

## Data Pipeline

TensorFlow's data pipeline is used to efficiently process the images.

The pipeline includes:

- Image loading
- Image preprocessing
- Label processing
- Dataset creation
- Batching
- Prefetching

This allows images to be prepared efficiently during training and validation.

## Model Training

The model is trained using the training dataset and validated using the validation dataset.

The training configuration includes:

- Adam optimizer
- Categorical Crossentropy loss
- Accuracy metric
- Early Stopping

## Early Stopping

Early Stopping is used to monitor validation performance during training.

It helps prevent unnecessary training and reduces overfitting by stopping the training process when validation performance stops improving.

## Model Evaluation

After training, the model is evaluated using the validation dataset.

The evaluation provides:

- Validation loss
- Validation accuracy

## Predictions

The trained model generates probability scores for each dog breed.

The breed with the highest probability is selected as the predicted breed.

The predictions are then mapped back to the corresponding dog breed names.

## Visualization

The project includes visualization of dog images together with their labels and predictions.

This helps to:

- Inspect model predictions
- Compare predicted and actual labels
- Identify incorrect predictions
- Understand model performance visually

## How to Run

### Option 1: Google Colab

1. Open the project notebook in Google Colab.
2. Download the Dog Breed Identification dataset from Kaggle.
3. Upload the dataset to Google Drive or Colab.
4. Mount Google Drive if the dataset is stored there.
5. Update the dataset path in the notebook.
6. Install any required libraries if they are not already available.
7. Run the notebook cells sequentially.
8. Train the model and evaluate its performance.
9. View the generated predictions and visualizations.

### Option 2: Local Jupyter Notebook

1. Clone the GitHub repository.
2. Download the Dog Breed Identification dataset from Kaggle.
3. Install Python and the required libraries.
4. Place the dataset in the appropriate local directory.
5. Update the dataset path in the notebook.
6. Open the notebook using Jupyter Notebook.
7. Run the cells sequentially.
8. Train and evaluate the model.
9. View the predictions and visualizations.

## Project Structure

    dog-breed-classification-mobilenetv2/
    │
    ├── Dog_Breed_Classification.ipynb
    ├── README.md
    └── .gitignore

The dataset is not included in the repository because of its large size.

## Results

The notebook provides model training and validation results, including:

- Training accuracy
- Validation accuracy
- Training loss
- Validation loss

The project also provides visualizations of dog images and model predictions.

The final accuracy can be updated here after completing the final training run.


## Future Improvements

Possible improvements for the project include:

- Fine-tuning the pretrained MobileNetV2 layers
- Adding more data augmentation
- Hyperparameter tuning
- Comparing MobileNetV2 with other pretrained CNN architectures
- Improving classification accuracy
- Adding confusion matrix analysis
- Adding precision, recall and F1-score
- Adding Top-5 accuracy
- Performing detailed error analysis
- Improving model generalization
- Deploying the model as a web application
- Creating an API for model predictions
- Converting the model to TensorFlow Lite for mobile or edge deployment

## How Future Improvements Can Be Added

Future development can be performed by:

1. Updating the preprocessing pipeline with additional augmentation techniques.
2. Unfreezing selected MobileNetV2 layers for fine-tuning.
3. Experimenting with different learning rates, batch sizes and optimizers.
4. Comparing the model with other pretrained architectures.
5. Adding additional evaluation metrics.
6. Analyzing incorrect predictions using a confusion matrix.
7. Saving the trained model for deployment.
8. Building a web interface where users can upload a dog image.
9. Creating an API to return the predicted breed and confidence score.
10. Optimizing the model for mobile or edge devices using TensorFlow Lite.

## Conclusion

This project demonstrates an end-to-end deep learning workflow for multi-class dog breed classification using TensorFlow, Keras and MobileNetV2.

It provides practical experience with image preprocessing, TensorFlow data pipelines, transfer learning, model training, evaluation, prediction and visualization.

## Author

**Ann Mary Thomas**



