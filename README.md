# Telco Customer Churn Prediction

## 🚀 Project Overview

This project is designed to analyze customer behavior and predict which telecom customers are likely to churn (i.e., leave the service). It combines exploratory data analysis (EDA), feature engineering, and machine learning modeling to:

Understand key factors influencing customer churn

Build and evaluate predictive models using Logistic Regression, Random Forest, and XGBoost

Apply techniques like SMOTE 

Provide actionable insights and business recommendations to help reduce churn rates

By understanding the patterns behind customer departure, this project aims not only to predict churn but also to assist in designing data-driven strategies to retain customers

---

## 📂 Dataset

* **Source**: Telco Customer Churn dataset
* **Files**:

  * `Telco-Customer-Churn.csv` (raw data)
  * `Telco-Customer-Churn-preprocessed.csv` (cleaned version)

The dataset used in this project is publicly available on Kaggle:  
[Telco Customer Churn - Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
---

## 💡 Process & Pipeline

### 1. Data Cleaning & Preprocessing

* Handled missing values
* Converted data types
* Encoded categorical variables
* Normalized continuous features

### 2. Exploratory Data Analysis (EDA)

* Investigated churn distribution
* Compared average charges & tenure
* Visualized patterns across senior citizens, internet service, and payment methods

### 3. Feature Engineering

Created new features to improve model performance:

* `short_term_customer` (based on tenure)
* `high_monthly_charge` (above median)
* `risk_score` (combination of multiple conditions)
* `avg_monthly_payment` (TotalCharges / Tenure)

### 4. Addressing Class Imbalance

Used **SMOTE** to oversample minority class (Churn = 1) to improve recall.

---

## 🎓 Models & Training

We trained and compared 3 different models:

### ✅ Models Used (Before & After SMOTE)

| Model               | Variants Tested                                     |
| ------------------- | --------------------------------------------------- |
| Logistic Regression | Before SMOTE, After SMOTE, With Feature Engineering |
| Random Forest       | Before SMOTE, After SMOTE                           |
| XGBoost             | Before SMOTE, After SMOTE, With Feature Engineering |

---

## 📊 Best Performance Results

| Model                                | Accuracy | Recall (Churn = 1) | F1-Score (Churn = 1) |
| ------------------------------------ | -------- | ------------------ | -------------------- |
| **XGBoost with Feature Engineering** | 0.80     | 0.68               | 0.62                 |
| Logistic Regression with SMOTE       | 0.80     | 0.56               | 0.60                 |
| Random Forest after SMOTE            | 0.79     | 0.63               | 0.64                 |

> Final model selection balances both precision and recall depending on business needs.

---

## 📁 Folder Structure

```
TELCO_CUSTOMER/
├── DataSet/
│   ├── Telco-Customer-Churn.csv
│   └── Telco-Customer-Churn-preprocessed.csv
├── Models/
│   ├── Best_Model_Logistic_Before_SMOTE.pkl
│   ├── Logistic_After_SMOTE.pkl
│   ├── RandomForest_After_SMOTE.pkl
│   ├── RandomForest_Before_SMOTE.pkl
│   ├── SecBestModel_XGboost_with_Feature.pkl
│   ├── xgboost_after_SMOTE.pkl
│   └── xgboost_Before_SMOTE.pkl
├── NoteBook/
│   ├── 01_EDA_Analysis.ipynb
│   ├── 02_Data_Preprocessing.ipynb
│   └── notebook.ipynb
├── requirements.txt
└── README.md
```

---

Abdulkarim Almalki
Linkdin : www.linkedin.com/in/abdulkarimalmalki
