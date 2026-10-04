# YUVA Internship Week 4 – Supervised Learning

## Project Title

Predicting Bank Term Deposit Subscription Using Supervised Machine Learning

## Objective

The objective of this project is to develop supervised machine learning models that predict whether a bank customer will subscribe to a term deposit.

## Dataset

The project uses the UCI Bank Marketing `bank-full.csv` dataset.

- Records: 45,211
- Original columns: 17
- Target variable: `y`
- Problem type: Binary Classification

The target contains two classes:

- `yes` – customer subscribed
- `no` – customer did not subscribe

## Methodology

The project follows these steps:

1. Dataset acquisition and exploration
2. Data quality analysis
3. Feature engineering
4. Categorical encoding
5. Numerical feature scaling
6. Stratified train-test split
7. Logistic Regression
8. Random Forest Classification
9. 5-fold stratified cross-validation
10. Model evaluation
11. Confusion matrix analysis
12. ROC-AUC analysis
13. Feature importance analysis
14. Model comparison

The `duration` feature was excluded because it represents the duration of the current contact and is only known after the interaction, which could introduce information leakage in a pre-contact prediction scenario.

## Feature Engineering

The following derived features were created:

- `age_group`
- `balance_category`
- `previous_contact`

## Models

### Logistic Regression

Used as the baseline classification model.

### Random Forest

Used as a nonlinear ensemble model and for feature importance analysis.

## Results

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 76.71% | **82.03%** |
| Precision | 28.20% | **34.91%** |
| Recall | **64.08%** | 62.00% |
| F1-Score | 39.17% | **44.67%** |
| ROC-AUC | 0.778 | **0.798** |

Random Forest achieved the strongest overall performance, while Logistic Regression achieved slightly higher recall.

## Cross-Validation

Stratified 5-fold cross-validation was used to evaluate model consistency.

Random Forest achieved an average ROC-AUC of approximately 0.789, compared with approximately 0.768 for Logistic Regression.

## Project Structure

```text
yuva-internship-supervised-learning
│
├── data
├── screenshots
├── output
├── Task_4_Supervised_Learning.ipynb
└── README.md
