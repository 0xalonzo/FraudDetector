# Fraud Detection Using Machine Learning

This project focuses on detecting fraudulent transactions in financial datasets using ensemble machine learning models. It employs data preprocessing techniques, Random Forest, Gradient Boosting, and an ensemble method to identify fraudulent transactions with high accuracy and reliability.

---

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Dataset Description](#dataset-description)
5. [Methodology](#methodology)
6. [Evaluation Metrics](#evaluation-metrics)
7. [Results](#results)

---
## Overview
Fraud detection is a critical task for financial institutions to minimize losses and protect customers. This project aims to solve the problem of detecting fraudulent transactions using machine learning techniques. By leveraging ensemble methods such as Random Forest and Gradient Boosting, this solution provides robust and interpretable results.
---

## Features
- **Data Preprocessing**:
  - Handling missing values using `SimpleImputer`.
  - Label encoding for categorical variables.
  - Feature scaling with `StandardScaler`.
- **Modeling**:
  - Random Forest for robust generalization.
  - Gradient Boosting for improved sensitivity to fraud cases.
  - Ensemble approach to combine model outputs.
- **Evaluation**:
  - Comprehensive evaluation using metrics such as accuracy, precision, recall, F1-score, ROC-AUC, and PR-AUC.
  - Visualizations of confusion matrices, ROC curves, and precision-recall curves.
---

## Technologies Used
- Python 3.x
- Libraries:
  - `pandas` for data manipulation.
  - `scikit-learn` for machine learning models and evaluation.
  - `matplotlib` for visualizations.
  - `numpy` for numerical computations.

---

## Dataset Description
The dataset contains transactional data with the following features:
- **amt**: Transaction amount.
- **lat, long**: Geographical coordinates of the transaction.
- **merch_lat, merch_long**: Merchant location coordinates.
- **merchant**: Name of the merchant.
- **category**: Type of transaction (e.g., travel, food).
- **city, state**: Transaction location details.
- **cc_num**: Credit card number (anonymized).
- **unix_time**: Timestamp of the transaction.
- **is_fraud**: Target variable indicating fraud (1) or non-fraud (0).

The dataset was preprocessed to handle missing values, encode categorical variables, and scale numerical features.
---

## Methodology

1. **Data Preprocessing**:
   - Missing values in `cc_num` and `unix_time` were filled with the most frequent values.
   - Categorical columns (`merchant`, `category`, `city`, `state`) were label-encoded.
   - Numerical features (`amt`, `lat`, `long`, `merch_lat`, `merch_long`) were standardized.

2. **Modeling**:
   - **Random Forest**: Built an ensemble of decision trees using bagging for robust predictions.
   - **Gradient Boosting**: Sequentially built trees focusing on correcting errors of previous trees.
   - **Ensemble Method**: Combined the predictions from Random Forest and Gradient Boosting using average probabilities.

3. **Evaluation**:
   - Metrics such as accuracy, ROC-AUC, precision, recall, and PR-AUC were used.
   - Confusion matrices and curve visualizations were generated for detailed insights.

---

## Evaluation Metrics
- **Accuracy**: Proportion of correctly classified transactions.
- **ROC-AUC**: Area under the Receiver Operating Characteristic curve, measuring the model's ability to separate fraud and non-fraud.
- **Precision**: Fraction of predicted fraud cases that are actual fraud.
- **Recall**: Fraction of actual fraud cases that were correctly identified.
- **PR-AUC**: Area under the Precision-Recall curve, focusing on minority class performance.

---

## Results
- **Random Forest**:
  - Accuracy: ~99%
  - ROC-AUC: ~0.99
  - PR-AUC: ~0.85
  - Strengths: High generalization, good performance across metrics.

- **Gradient Boosting**:
  - Accuracy: ~98%
  - ROC-AUC: ~0.98
  - PR-AUC: ~0.87
  - Strengths: Better sensitivity to subtle fraud patterns.

- **Ensemble Method**:
  - Combined the strengths of both models for more balanced predictions.
  - Showed improved precision and recall for fraud detection.
---
Created by: Alonzo Garcia and Steve Martinez
