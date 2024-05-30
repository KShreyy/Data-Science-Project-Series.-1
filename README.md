This repository contains a machine learning model to predict breast cancer using a Support Vector Machine (SVM) and feature selection via Recursive Feature Elimination (RFE). The dataset used is from a CSV file containing various features of breast cancer tumors.

Table of Contents

Requirements
Dataset
Data Preprocessing
Feature Selection
Model Training and Evaluation
Usage
Results

Requirements
        Python 3.x
        pandas
        scikit-learn


Dataset
      The dataset should be in a CSV file named data.csv with the following columns:

     id: Unique identifier for each tumor
     diagnosis: Diagnosis of the tumor (M = Malignant, B = Benign)
     Other columns representing various features of the tumors (e.g., radius, texture, perimeter, area, smoothness, etc.)
Data Preprocessing
     Handle Missing Values: Any missing values in the dataset are dropped.
     Encode Target Variable: The diagnosis column is encoded where 'M' (Malignant) is mapped to 1 and 'B' (Benign) is mapped to 0.
Feature Scaling: Features are standardized using StandardScaler to have zero mean and unit variance.
     Feature Selection
     Recursive Feature Elimination (RFE) with a linear SVM is used to select the top 10 features from the dataset. You can adjust the number of features to select by modifying the n_features_to_select parameter.

Model Training and Evaluation
Train-Test Split: The dataset is split into training and testing sets using an 80-20 split.
Model Training: An SVM model is trained on the selected features of the training set.
Model Evaluation: The model's performance is evaluated using accuracy and confusion matrix metrics on the test set.
