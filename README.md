# **Cardio Health Risk Prediction Using Logistic Regression**

## **Table of Contents**
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
- [Results](#results)
- [Future Work](#future-work)

## **Project Overview**
This project focuses on predicting the presence of heart disease in patients using a Logistic Regression model. The model is trained on a dataset containing various health indicators like age, cholesterol levels, blood pressure, and others, aiming to classify whether or not a patient is at risk of heart disease.

## **Dataset**
The dataset used for this project consists of patient records with the following attributes:
- **Age**: The patient's age
- **Sex**: Gender (1 = male, 0 = female)
- **Chest pain type**: Type of chest pain (1–4 types)
- **Blood Pressure (BP)**: Resting blood pressure (in mm Hg)
- **Cholesterol**: Serum cholesterol (in mg/dl)
- **Fasting Blood Sugar (FBS over 120)**: Whether fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
- **Electrocardiographic results (EKG results)**: Results of the electrocardiogram (0-2)
- **Max HR**: Maximum heart rate achieved
- **Exercise Angina**: Exercise-induced angina (1 = yes, 0 = no)
- **ST Depression**: ST depression induced by exercise relative to rest
- **Slope of ST**: The slope of the peak exercise ST segment (1-3)
- **Number of Vessels Fluoroscopy**: Number of major vessels (0-3) colored by fluoroscopy
- **Thallium Stress Test**: Result of thallium stress test (3, 6, or 7)
- **Heart Disease Presence**: Target label indicating the presence of heart disease (True/False)

There are a total of 270 records with 14 features.

## **Data Preprocessing**
The following steps were performed on the dataset to prepare it for modeling:
1. **Handling Missing Values**: The dataset was checked for missing values, and no missing data was found.
2. **Categorical Variables**: The target variable, `Heart Disease`, was converted into a binary indicator (0 for no disease, 1 for disease).
3. **Train-Test Split**: The dataset was split into training and testing sets (75% training, 25% testing).
4. **Feature Scaling**: Standardization was not explicitly performed but can be added if required.

## **Model Building**
A Logistic Regression model was built using `scikit-learn`. The following steps were followed:
1. **Model Initialization**: Logistic Regression with `max_iter=750`.
2. **Model Training**: The model was trained on the training set using `X_train` and `y_train`.
3. **Prediction**: Predictions were made on the test set using the trained model.
4. **Evaluation**: The model's performance was evaluated using the following metrics:
   - Confusion matrix
   - Accuracy score
   - Classification report (Precision, Recall, F1-Score)

## **Results**
The Logistic Regression model achieved an accuracy of **89.7%** on the test dataset. Below is the confusion matrix for the predictions:

```
Confusion Matrix:
[[37,  3],
 [ 4, 24]]
```

- **Precision**: How many selected items are relevant?
- **Recall**: How many relevant items are selected?
- **F1-Score**: Harmonic mean of precision and recall

## **Future Work**
- **Feature Engineering**: Improve the model by performing feature scaling, handling outliers, and performing feature selection.
- **Hyperparameter Tuning**: Use techniques like grid search to tune hyperparameters for better performance.
- **Model Comparison**: Compare Logistic Regression with other classification algorithms like Random Forest, SVM, or Neural Networks.
