# Credit Card Fraud Detection

A machine learning project to detect fraudulent credit card transactions using supervised classification techniques. The project focuses on handling severe class imbalance and evaluating models using appropriate metrics such as ROC-AUC and Precision-Recall curves.

## Problem Statement

Financial institutions process millions of transactions daily, with fraudulent transactions representing a very small fraction of total activity. Detecting fraud accurately while minimizing false alarms is critical.

This project builds a classification model to:

- Identify fraudulent transactions

- Handle extreme class imbalance

- Optimize recall without excessively harming precision

- Interpret model behavior through feature importance analysis

## Dataset:

Source: Kaggle Fraud Detection Dataset

Total Records: 1,296,675

Fraud Percentage: 0.57%

Features include:

- Transaction amount

- Merchant category

- Timestamp

- Customer demographics

- Geographic information

# Project Workflow:
## 1.) Data Preprocessing:

- Removed high-cardinality and leakage features (e.g., card numbers, names, transaction IDs)

- Extracted time-based features (hour, day, month)

- Converted date of birth to age

- One-hot encoded categorical variables

- Stratified train-test split to preserve class distribution

## 2.) Handling Class Imbalance:

- Used class_weight='balanced' in models

- Evaluated using Precision-Recall curve (more suitable than accuracy)

## 3.) Models Implemented:

- Logistic Regression
- Random Forest Classifier

# Model Performance:
## Logistic Regression

- ROC-AUC: 0.915
- Fraud Recall: 76%
- Fraud Precision: 4%

Baseline model with high recall but excessive false positives.

## Random Forest (Primary Model)

- ROC-AUC: 0.984
- Average Precision Score: 0.773
- Fraud Recall: 89%
- Fraud Precision: 23%

Strong performance on a highly imbalanced dataset.

# Precision–Recall Analysis:

Precision-Recall curve used instead of relying on accuracy.

Demonstrates trade-off between detecting more fraud (recall) and reducing false alarms (precision).

Lowering threshold from 0.5 to 0.3:

Recall increased to 97%

Precision dropped to 4%

This highlights the importance of threshold selection based on business cost considerations.

# Feature Importance (Random Forest):

### Top influential features:

- Transaction Amount (amt)
- Hour of Transaction
- Shopping (Online)
- Grocery POS
- Gas & Transport
- Age
- Miscellaneous categories

These results align with real-world fraud behavior patterns.

# Evaluation Metrics Used:

- ROC-AUC
- Precision-Recall Curve
- Average Precision Score
- Classification Report
- Confusion Matrix
- Feature Importance:

Accuracy was intentionally not used as the primary metric due to class imbalance.

# Business Interpretation:

The model demonstrates strong discriminative ability on a highly imbalanced dataset.

In real-world deployment:

- Lower thresholds increase fraud detection but raise customer friction.
- Higher thresholds reduce false positives but may miss fraudulent activity.

The optimal threshold depends on:

- Cost of missed fraud
- Cost of blocking legitimate transactions

# Key Learnings:

- Handling imbalanced datasets effectively
- Importance of Precision-Recall over accuracy
- Threshold tuning for business-driven optimization
- Feature engineering for structured financial data

# Tech Stack:

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- KaggleHub

# How to Run:

- Install dependencies
- Download dataset via KaggleHub
- Run notebook top-to-bottom
- Evaluate models and visualizations
