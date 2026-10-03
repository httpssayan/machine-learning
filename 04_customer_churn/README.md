# Customer Churn Prediction

## Overview

A machine learning project that predicts whether a telecom customer
will churn based on customer demographics, services, contract details,
and billing information.

## Problem

Customer churn is a binary classification problem:

- 0 → No Churn
- 1 → Churn

The goal is to identify customers who are likely to leave the service.

## Workflow

1. Data loading
2. Exploratory Data Analysis
3. Data cleaning
4. Handling missing values
5. Feature preprocessing
6. Categorical encoding
7. Train-test split
8. Decision Tree classification
9. Model evaluation
10. Hyperparameter tuning
11. Feature importance analysis
12. Final evaluation

## Preprocessing

### Numerical Features
- Missing-value imputation
- Median strategy

### Categorical Features
- Missing-value imputation
- One-Hot Encoding
- Unknown categories handled safely

### Additional Cleaning
`TotalCharges` was converted from string/object to numeric.

## Model

Decision Tree Classifier.

Hyperparameters were optimized using:

- GridSearchCV
- 5-fold Cross Validation
- ROC-AUC scoring

## Results

| Metric | Result |
|---|---:|
| Test Accuracy | ~77.5% |
| Test ROC-AUC | ~81.6% |
| Churn Precision | ~60% |
| Churn Recall | ~47% |
| Churn F1 | ~53% |

## Important Observation

The model identifies non-churning customers more effectively than
churning customers.

This demonstrates why accuracy alone should not be used to evaluate
imbalanced classification problems.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Concepts Practiced

- Decision Trees
- Gini Impurity
- Entropy
- Information Gain
- Feature Importance
- Pipelines
- ColumnTransformer
- Cross Validation
- GridSearchCV
- ROC-AUC
- Confusion Matrix
- Precision
- Recall
- F1 Score