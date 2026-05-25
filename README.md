# computer-vision

# Midterm Project - Image Classification with Machine Learning Pipeline

## Student Information
Name: MOH SYURIL ISWAN  
NIM: 4222301069  
Class: A MALAM  

## Project Overview
This project implements an image classification system using the EMNIST Letters dataset with a Machine Learning Pipeline approach. The system uses Histogram of Oriented Gradients (HOG) for feature extraction and Support Vector Machine (SVM) for classification.

## Dataset
Dataset used: EMNIST Letters Dataset  
Source: Kaggle EMNIST Dataset  

The dataset contains handwritten letter images with:
- Image size: 28 x 28 pixels
- 26 classes (A-Z)
- 100 samples per class
- Total dataset used: 2600 samples

## Project Pipeline

### 1. Dataset Preparation
- Load EMNIST Letters dataset
- Select 100 samples for each class
- Create balanced dataset
- Shuffle dataset
- Split dataset into:
  - 80% training
  - 20% testing

### 2. Data Visualization
- Reshape image into 28 x 28
- Correct EMNIST image orientation
- Display sample images

### 3. Feature Extraction
Use Histogram of Oriented Gradients (HOG) with customized parameters:
- orientations = 12
- pixels_per_cell = (8,8)
- cells_per_block = (2,2)
- block_norm = L2-Hys

### 4. Classification
Use Support Vector Machine (SVM) with Grid Search parameter tuning:
- Kernel: linear, rbf, poly
- C: 0.1, 1, 10, 100
- Gamma: scale, auto, 0.001, 0.01

### 5. Evaluation
Performance metrics used:
- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

## Libraries Used
- NumPy
- Pandas
- Matplotlib
- Seaborn
- scikit-image
- scikit-learn

## Project Structure

```text
computer-vision/
│── emnist-letters-train.csv
│── emnist_hog_svm_classification.ipynb
│── README.md
│── results/