# Loan_Default_Prediction_Analysis

# Loan Default Prediction using Logistic Regression, Random Forest & XGBoost

## Overview

This project aims to predict whether a loan applicant will **default** or **repay** a loan using supervised machine learning models.  
Three algorithms were implemented and compared:

- Logistic Regression  
- Random Forest  
- XGBoost  

The target variable is:

- **1** → Loan Default  
- **0** → Loan Repaid  

The focus of this project is not only on prediction accuracy, but also on understanding how **data characteristics** influence model behavior.

---

## Dataset

The dataset contains financial and demographic information about loan applicants, including:

- Loan amount  
- Interest rate  
- Income  
- Employment length  
- Credit history  
- Loan purpose  
- Loan status  

The `loan_status` column was converted into a binary target:

- Default-related statuses → 1  
- Fully paid → 0  

The dataset is **highly imbalanced**, with far more non-default cases than defaults.

---

## Methodology

1. Data loading and exploration  
2. Handling missing values  
3. Encoding categorical variables  
4. Feature scaling (for Logistic Regression)  
5. Train-test split  
6. Model training  
7. Performance evaluation  

All models were trained using the same preprocessing pipeline to ensure fair comparison.

---

## Models Used

### Logistic Regression  
A linear and interpretable baseline model commonly used in credit risk analysis.

### Random Forest  
An ensemble model capable of capturing non-linear relationships and feature interactions.

### XGBoost  
A gradient boosting model optimized for performance on structured tabular data.

---

## Evaluation Metrics

Due to class imbalance, the following metrics were used:

- Precision  
- Recall  
- F1-score  
- ROC-AUC  

Accuracy alone is not a reliable metric for loan default prediction.

---

## Results

All three models produced **very similar performance metrics** and prediction behavior.

| Model | Precision | Recall | F1-score | ROC-AUC |
|------|-----------|--------|----------|---------|
| Logistic Regression | Similar | Similar | Similar | Similar |
| Random Forest | Similar | Similar | Similar | Similar |
| XGBoost | Similar | Similar | Similar | Similar |

---

## Why Were the Results Similar?

This outcome is expected due to the following factors:

### 1. Class Imbalance  
Most loan records belong to the non-default class.  
Models learn that predicting the majority class leads to high accuracy.

### 2. Probability Threshold  
Predictions were converted using a 0.5 threshold.  
Different probability scores can still produce the same final label.

### 3. Limited Feature Separation  
If features do not strongly distinguish defaulters from non-defaulters, all models reach similar conclusions.

### 4. Same Preprocessing Pipeline  
All models were trained on the same cleaned and encoded data, leading to similar input representations.

---

## Key Insight

The dataset structure had a stronger influence on model behavior than the choice of algorithm.  
This highlights the importance of **data quality, class balance, and feature engineering** in credit risk modeling.

---

## Project Structure

