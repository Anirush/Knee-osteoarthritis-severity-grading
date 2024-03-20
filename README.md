Deep Learning Model for Knee Classification
This repository contains code for a deep learning model aimed at classifying knee images into different categories: Healthy, Doubtful, Moderate, and Severe. Below is an overview of the project structure and key components:

Project Structure:
README.md: Overview and instructions for running the code.
main.py: Python script containing the code for model training and evaluation.
requirements.txt: List of Python dependencies required to run the code.
Instructions:
Setup Environment:

Ensure you have Python installed (preferably Python 3.x).
Install required dependencies using pip install -r requirements.txt.
Dataset Preparation:
get a dataset from kaggle
Organize your dataset into three folders: train, test, and val, each containing subfolders for different classes (Healthy, Doubtful, Moderate, Severe).
Training the Model:

Run the main.py script.
The script will load the dataset, preprocess images, train the model, and evaluate its performance.
Model Evaluation:

The script generates a classification report and confusion matrix to evaluate the model's performance on the test dataset.
Model Saving:

After training, the model is saved as a .h5 file for future use.
Key Components:
Data Preprocessing: The script preprocesses images, including resizing, augmentation, and normalization, using TensorFlow's ImageDataGenerator.
Model Architecture: The model architecture is based on transfer learning using pre-trained MobileNetV2 and EfficientNetB5 models, with additional dense layers for classification.
Callbacks: Custom callback LR_ASK is used to dynamically adjust learning rate and stop training based on user input during training.
Training and Evaluation: The model is trained using the Adamax optimizer and categorical cross-entropy loss. Evaluation metrics include accuracy, loss, classification report, and confusion matrix.
Model Saving: After training, the model is saved for future use.
