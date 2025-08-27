# Customer Churn Prediction

![Accuracy](https://img.shields.io/badge/Accuracy-0.990-brightgreen)
![Precision](https://img.shields.io/badge/Precision-0.974-blue)
![Recall](https://img.shields.io/badge/Recall-0.989-orange)
![F1 Score](https://img.shields.io/badge/F1_Score-0.981-red)

This project implements a **Customer Churn Prediction** model using machine learning techniques. The goal is to predict whether a customer will churn (leave) a service based on historical customer data.

The dataset was imported from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) and contains information about customer demographics, services, and account details.

---

## Project Overview

### Data Handling
- Missing values were addressed and categorical features were encoded to numeric values suitable for machine learning models.
- Features such as `Contract`, `PaymentMethod`, and `gender` were mapped to numerical values.

### Handling Data Imbalance
- The dataset is imbalanced (more non-churners than churners).
- **SMOTE (Synthetic Minority Oversampling Technique)** was used to oversample the minority class and balance the dataset for model training.

### Model Training and Evaluation
Three models were trained and evaluated on the same dataset:
1. Random Forest Classifier (RFC)
2. Logistic Regression
3. XGBoost Classifier

Metrics used for evaluation include **Accuracy, Precision, Recall, and F1-Score**.

### Model Selection
Although all three models were tested, **XGBoost was selected** due to its realistic evaluation scores and excellent balance between precision and recall.

---

## XGBoost Model Performance

| Metric     | Score |
|-----------|-------|
| Accuracy  | 0.990 |
| Precision | 0.974 |
| Recall    | 0.989 |
| F1 Score  | 0.981 |

---

## Usage

- Load the dataset (CSV file imported from Kaggle).  
- Preprocess data: encode categorical features and handle missing values.  
- Handle data imbalance with **SMOTE**.  
- Train and evaluate models (RFC, Logistic Regression, XGBoost).  
- Select XGBoost for predictions on new customers.

---

## Dataset

- Source: [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- Contains 21 features including customer demographics, account info, and usage metrics.  
- Target variable: `Churn` (0 = No churn, 1 = Churn)  

---

## Conclusion

This project demonstrates a complete **machine learning workflow**:

1. Data cleaning and preprocessing  
2. Handling imbalanced datasets  
3. Model training and evaluation  
4. Model selection based on realistic metrics  

**XGBoost** emerged as the best model for predicting customer churn with strong precision, recall, and overall accuracy.
