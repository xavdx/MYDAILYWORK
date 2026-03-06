# Customer Churn Prediction:

## Overview:

Customer churn prediction is a critical problem for subscription-based businesses and financial institutions. Identifying customers who are likely to leave allows companies to take proactive retention actions.

This project builds a machine learning pipeline to predict whether a bank customer will churn using demographic and account-related features. Multiple models were trained and evaluated, and the final model was interpreted using SHAP explainability to understand the factors influencing churn.

## Dataset:

Source: Kaggle- Bank Customer Churn Prediction

The dataset contains information about 10,000 bank customers including demographic attributes, financial details, and account behavior.

## Features:

- CreditScore

- Geography

- Gender

- Age

- Tenure

- Balance

- NumOfProducts

- HasCrCard

- IsActiveMember

- EstimatedSalary

## Target Variable:

### Exited

0 → Customer stayed

1 → Customer churned

## Project Workflow:

The project follows a complete machine learning workflow:

- Data Loading

- Exploratory Data Analysis (EDA)

- Data Preprocessing

- Model Training

- Model Evaluation

- Hyperparameter Tuning

- Model Explainability

- Customer Risk Segmentation

## Exploratory Data Analysis:
 
 EDA was performed to understand patterns in customer churn behavior.

## Key visualizations included:

- Churn distribution

- Geography vs churn

- Gender vs churn

- Correlation heatmap

## Key Observations:

- Customers located in Germany have a higher churn rate.

- Inactive customers churn significantly more often.

- Customers with fewer bank products are more likely to churn.

# Data Preprocessing:

Several preprocessing steps were applied before model training.

- Removed Irrelevant Columns

- RowNumber

- CustomerId

- Surname

## Feature Scaling:

- StandardScaler was applied to numerical features.

## Categorical Encoding:

OneHotEncoder was used for:

- Geography

- Gender

A ColumnTransformer pipeline was used to ensure consistent preprocessing during training and testing.

## Machine Learning Models:

Three machine learning models were trained and evaluated.

- Logistic Regression

- Baseline linear classification model.

- Random Forest

Tree-based ensemble model capable of capturing nonlinear relationships.

Gradient Boosting

Boosting-based model that sequentially improves prediction errors.

## Model Performance:
Model	              Accuracy	ROC-AUC
Logistic Regression	~0.81	    ~0.77
Random Forest	      ~0.86	    ~0.85
Gradient Boosting	   0.87	     0.87

Gradient Boosting achieved the best performance and was selected as the final model.

## Hyperparameter Tuning:

Hyperparameter tuning was performed using GridSearchCV with ROC-AUC as the evaluation metric.

The optimal parameters were found to match the default Gradient Boosting settings, indicating that the baseline model was already well suited to the dataset.

## Model Evaluation:

Several evaluation techniques were used.

- Confusion Matrix Metrics

- Precision

- Recall

- F1-score

- ROC Curve

Used to evaluate classification performance across different probability thresholds.

## Precision-Recall Curve:

This metric is particularly useful for imbalanced datasets such as churn prediction.

# Feature Importance:

Feature importance analysis identified the most influential variables affecting churn.

## Top features include:

- Age

- Number of products

- Account balance

- Credit score

- Estimated salary

# Model Explainability (SHAP):

SHAP (SHapley Additive exPlanations) was used to understand how each feature influences model predictions.

### SHAP helps explain:

- Which features influence churn predictions

- Whether they increase or decrease churn probability

- The magnitude of each feature's impact

### Key Insights: 

- Customers with fewer bank products have higher churn risk.

- Older customers are more likely to churn.

- Inactive members strongly increase churn probability.

- Customers located in Germany show higher churn likelihood.

# Customer Risk Segmentation:

Instead of only predicting churn, customers were categorized into risk groups based on churn probability.

## Risk Categories:

- Low Risk → Probability < 0.30

- Medium Risk → Probability between 0.30 and 0.60

- High Risk → Probability > 0.60

This segmentation enables businesses to prioritize retention strategies.

## Example Retention Strategy:

### High Risk:

- Targeted retention campaigns

- Personalized support outreach

### Medium Risk:

- Loyalty incentives

- Engagement programs

### Low Risk:

- Regular customer engagement

## Technologies Used:

- Python

- Pandas

- NumPy

- Scikit-learn

- Matplotlib

- Seaborn

- SHAP

- Google Colab

### Project Structure:
Task_3_Customer_Churn_Prediction
│
├── Task_3_Customer_Churn_Prediction.ipynb
└── README.md

# Conclusion:
This project demonstrates a complete machine learning pipeline for customer churn prediction including data preprocessing, model training, evaluation, explainability, and business-oriented risk segmentation.

The final Gradient Boosting model achieved an ROC-AUC score of approximately 0.87, and SHAP analysis provided valuable interpretability for understanding the drivers of customer churn.
