# Machine Learning Internship Tasks

This repository contains the projects completed as part of a **Machine Learning Internship**.  
The objective of these tasks was to build practical machine learning solutions using real-world datasets.

The projects covers three tasks: **credit card fraud detection, customer churn prediction, and character-level text generation using RNNs**.

---

# Repository Structure:
MYDAILYWORK
│

├── Task_2_Credit_Card_Fraud_Detection

│ ├── Task_2_Credit_Card_Fraud_Detection.ipynb

│ └── README.md

│

├── Task_3_Customer_Churn_Prediction

│ ├── Task_3_Customer_Churn_Prediction.ipynb

│ └── README.md

│

├── Task_5_Handwritten_Text_Generation

│ ├── Task_5_Text_Generation.ipynb

│ └── README.md

│

└── README.md


Each task folder contains:
- The project notebook
- A detailed project-specific README

---

# Completed Tasks:

## 1️.) Credit Card Fraud Detection:

**Objective:**  
Build a machine learning model to detect fraudulent credit card transactions.

**Key Steps:**
- Data preprocessing and cleaning
- Handling class imbalance
- Feature engineering
- Model training and evaluation

**Models Used:**
- Logistic Regression
- Random Forest Classifier

**Evaluation Metrics:**
- ROC-AUC
- Precision–Recall Curve
- Confusion Matrix
- Feature Importance Analysis

**Key Result:**
Random Forest achieved strong fraud detection performance on a highly imbalanced dataset.

**Project Folder:**  
`Task_2_Credit_Card_Fraud_Detection`

---

## 2️.) Customer Churn Prediction:

**Objective:**  
Predict whether a bank customer is likely to leave the service.

**Key Steps:**
- Data exploration and preprocessing
- Feature engineering
- Model training and evaluation

**Models Used:**
- Logistic Regression
- Random Forest
- Gradient Boosting

**Evaluation Metrics:**
- Accuracy
- Precision / Recall
- ROC-AUC
- Confusion Matrix

**Key Result:**
The model successfully identified customer churn patterns based on customer behavior and demographic data.

**Project Folder:**  
`Task_3_Customer_Churn_Prediction`

---

## 3️.) Handwritten Text Generation using RNN:

**Objective:**  
Train a **character-level Recurrent Neural Network (RNN)** to generate text based on handwritten text examples.

**Dataset:**
IAM Handwriting Dataset (text transcriptions from handwritten samples)

**Model Architecture:**
- Embedding Layer
- LSTM (128 units)
- Dropout
- Dense Softmax Output

**Training Configuration:**
- Sequence Length: 40 characters
- Batch Size: 128
- Epochs: 30

**Key Result:**
The model learned character patterns and generated new text sequences resembling the training corpus.

**Project Folder:**  
`Task_5_Handwritten_Text_Generation`

---

# Technologies Used:

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Seaborn
- HuggingFace Datasets
- Google Colab

---

# Skills Demonstrated:

- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Handling Imbalanced Datasets
- Machine Learning Model Development
- Deep Learning (RNN / LSTM)
- Model Evaluation & Interpretation
- Text Generation using Neural Networks

---

# Note:

The dataset link provided in the internship instructions for the **Handwritten Text Generation task** redirected to the HuggingFace *Trending Papers* page instead of an actual dataset.  
Therefore, the **IAM Handwriting Dataset** was used via the HuggingFace datasets library to obtain handwritten text transcriptions for model training.
