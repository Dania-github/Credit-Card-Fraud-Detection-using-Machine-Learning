**💳 Credit Card Fraud Detection using Machine Learning**

**📌 Project Overview**

This project focuses on detecting fraudulent credit card transactions using supervised machine learning techniques.

Credit card fraud detection is a highly imbalanced classification problem where fraudulent transactions represent a very small fraction of total transactions. The goal is to build a model that maximizes fraud detection (Recall) while minimizing false alarms (Precision).

📂 **Dataset**

The dataset contains anonymized transaction data including:

PCA-transformed features (V1 – V28)

Time (seconds elapsed between transactions)

Amount (transaction value)

Class (Target Variable)

0 → Non-Fraud

1 → Fraud

⚠️ The dataset is highly imbalanced (~0.17% fraud cases).

**🧠 Problem Statement**

Build a robust classification model that:

Detects fraudulent transactions accurately

Handles severe class imbalance

Avoids overfitting

Uses appropriate evaluation metrics beyond accuracy

**🔎 Exploratory Data Analysis (EDA)**

Performed the following steps:

Checked class distribution

Analyzed feature distributions (Amount, Time)

Identified skewness and outliers

Generated correlation matrix

Observed low multicollinearity due to PCA transformation

Key Insight:

Accuracy is not an appropriate metric due to extreme imbalance.

**⚙️ Data Preprocessing**

Stratified Train-Test Split

Feature Scaling using StandardScaler

Handled class imbalance using:

class_weight='balanced'

(Optional) SMOTE oversampling

Important:
Scaler was fit only on training data to prevent data leakage.

**🤖 Models Implemented**

Logistic Regression (Baseline)

(Optional) Random Forest

(Optional) Gradient Boosting / XGBoost

**📊 Evaluation Metrics**

Since this is an imbalanced classification problem, the following metrics were used:

Precision

Recall

F1-Score

ROC-AUC

Precision-Recall Curve

Confusion Matrix (Raw + Normalized)

**Special Focus**:

Minimize False Negatives (missed fraud cases)

Balance Precision vs Recall tradeoff

**📈 Model Evaluation**

Plotted ROC Curve

Plotted Precision-Recall Curve

Compared models based on:

Recall (Fraud class)

F1-score

PR-AUC

Precision-Recall curve was prioritized due to class imbalance.

**🛠️ Tech Stack**

Python 3.10

Pandas

NumPy

Scikit-learn

Seaborn

Matplotlib

Imbalanced-learn (optional)

## 📁 Project Structure

```bash
Credit_Card_detection/
│
├── dataset/                  # Raw dataset files
│   └── creditcard.csv
│
├── notebooks/                # Jupyter notebooks
│   └── credit_card.ipynb
│
├── models/                   # Saved trained models (optional)
│   └── random_forest.pkl
│
├── requirements.txt          # Project dependencies
├── README.md                 # Project documentation
└── venv/                     # Virtual environment (not pushed to GitHub)
```
