# Quantum Transfer Learning for Medical Image Classification

## Project Overview

This project explores the use of quantum machine learning for medical image classification by combining classical deep learning with a quantum classifier. It uses a pretrained ResNet18 model for feature extraction and a Variational Quantum Classifier (VQC) to classify chest X-ray images into Normal and Pneumonia categories.

The project also compares the quantum classifier with a classical machine learning classifier using the same reduced feature representation.

## Problem Statement

Medical image classification using deep learning can require significant computational resources. This project investigates whether a hybrid quantum-classical approach can be used for binary medical image classification by combining pretrained feature extraction with a compact quantum classification circuit.

## Objectives

- Use transfer learning to extract meaningful features from chest X-ray images.
- Reduce the extracted features to a four-dimensional representation.
- Encode the reduced features into a four-qubit quantum circuit.
- Implement a Variational Quantum Classifier for binary classification.
- Compare quantum and classical classifiers using the same input features.
- Evaluate classification performance using appropriate metrics.

## Dataset

**Dataset:** PneumoniaMNIST from MedMNIST

The dataset contains grayscale chest X-ray images for two classes:

- Normal
- Pneumonia

The images are preprocessed and resized to meet the input requirements of the pretrained ResNet18 feature extractor.

Dataset information: https://medmnist.com/

## Methodology

### 1. Data Loading and Preprocessing
Load the PneumoniaMNIST dataset and prepare the chest X-ray images for feature extraction.

### 2. ResNet18 Feature Extraction
Use a pretrained ResNet18 model to extract visual features from the input images.

### 3. Feature Reduction
Reduce the extracted feature representation to four numerical values for use by the quantum circuit.

### 4. Quantum Encoding
Encode the four reduced features into a quantum circuit using four qubits.

### 5. Variational Quantum Classifier
Apply trainable quantum gates and measurements to produce outputs for Normal and Pneumonia classification.

### 6. Classical Baseline and Evaluation
Compare the quantum classifier with a conventional classical classifier trained on the same reduced features.

## System Architecture

Chest X-ray Images
        ↓
Data Preprocessing
        ↓
Pretrained ResNet18
        ↓
Feature Extraction
        ↓
Feature Reduction (4 Features)
        ↓
Quantum Encoding (4 Qubits)
        ↓
Variational Quantum Classifier
        ↓
Classification Output

A classical classifier using the same reduced features serves as the baseline for comparison.

## Technologies Used

- Python
- Google Colab
- PyTorch
- Torchvision
- PennyLane
- MedMNIST
- NumPy
- Scikit-learn
- Matplotlib

## Evaluation Metrics

The project can evaluate classification performance using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- Class-wise Performance

Accuracy alone may not fully represent model performance when the classes are imbalanced, so additional evaluation metrics are important.

## How to Run

1. Download or clone this repository.
2. Open `quantum_transfer_learning.ipynb` in Google Colab or Jupyter Notebook.
3. Install the required libraries specified in the notebook.
4. Load the PneumoniaMNIST dataset.
5. Execute the notebook cells in order.
6. Review the classification outputs and evaluation metrics produced by the notebook.

The notebook and its dependencies may require adjustments depending on the runtime environment.

## Expected Outcome

The project aims to evaluate the feasibility of using a hybrid quantum-classical classification approach for chest X-ray images and compare its performance with a classical baseline.

The actual performance and any potential advantages of the quantum classifier must be established through experimental evaluation.

## Project Status

In Progress


