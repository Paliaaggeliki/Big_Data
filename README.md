# Big_Data: Classification of Diabetes

<p align="center">
  <img src="https://www.modelateapps.com/upload/ckeditor/0f4631b9694864f02be81cde06bbf93a.gif" width="500">
</p>

This project classifies diabetes based on various medical features using machine learning techniques. The steps in the project include data preprocessing, model training, and evaluation. The primary goal is to predict whether a person has diabetes based on medical features such as BMI, blood glucose levels, HbA1c levels, and other health-related information.

The dataset used in this project contains **100,000 rows** and **16 columns**. Each row represents an individual medical record, and the columns include various features related to the patient's health status. The dataset is used for classifying whether a person has diabetes or not, based on these features.

## Project Overview

The project is divided into the following stages:

### 1. Data Preprocessing
- **Handling Missing Values**: Missing values in the dataset, such as "No Info" in the `smoking_history` column, are replaced by the most frequent value.
- **Outlier Detection and Removal**: Outliers in numerical columns like `bmi`, `hbA1c_level`, and `blood_glucose_level` are detected and removed using the Interquartile Range (IQR) method.
- **Normalization**: Features like `bmi`, `hbA1c_level`, and `blood_glucose_level` are normalized to a [0, 1] range using Min-Max scaling.
- **Feature Selection**: Categorical features (`gender`, `location`, and `smoking_history`) are encoded using `LabelEncoder`, and the most relevant features are selected for training.

### 2. Machine Learning Algorithms
- **Random Forest Classifier**: An ensemble model using decision trees.
- **Decision Tree Classifier**: A basic tree-based model for classification.
- **Cross-Validation**: Stratified K-Fold Cross-Validation (5 splits) ensures the model's performance is evaluated reliably.
- **Train-Test Split**: The dataset is split into training and testing sets with different ratios (e.g., 90/10, 80/20).

### 3. Model Evaluation
The models are evaluated using the following metrics:
- **Accuracy**: Percentage of correct predictions.
- **Precision, Recall, F1-Score**: Evaluate the classification of positive and negative instances.
- **ROC-AUC**: Area under the Receiver Operating Characteristic curve.
