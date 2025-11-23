## Overview

This project analyzes a synthetic dataset of e-commerce transactions to explore how fraudulent behavior can be identified using data patterns.
It includes:

1. Exploratory Data Analysis (EDA)

2. Visualizations to understand transaction behavior

3. Creating new meaningful features

4. Addressing class imbalance

5. Training a Random Forest classifier as a baseline model

6. Evaluating performance and identifying improvement opportunities

## Exploratory Data Analysis

The dataset contains 23,634 transactions with 5% labeled as fraudulent.
Key steps in the analysis:

1. Visualizing transaction amounts, customer ages, device types, payment methods, and product categories

2. Identifying skewed distributions, outliers, and anomalies

3. Understanding imbalance between fraud and non-fraud

4. Reviewing correlations between numerical features

5. These visual insights helped guide the next stage of the project.

## New Feature Creation

To capture useful patterns, several additional features were created:

1. Address_Mismatch — different shipping and billing addresses

2. Transaction_Weekday — day of the week the transaction occurred

3. Transaction_Hour — hour of transaction

4. Customer_Frequency — how often the customer appears

5. Amount_Higher_Than_Average — whether the transaction amount exceeds the category’s average

6. These added context for each transaction beyond what the raw dataset provided.

## Machine Learning Model

A Random Forest classifier was used as a baseline model, with:

1. Balanced class weights

2. Stratified train/test split

3. Label encoding for categorical variables

## Model Highlights:

Accuracy: 97%

Precision (Fraud): 95%

Recall (Fraud): 36%

F1-Score (Fraud): 52%

## What This Means:

The model is very good at correctly identifying fraud when it predicts it, but it still misses many fraudulent cases — a common challenge with imbalanced datasets.

## This opens the door to future improvements such as:

1. SMOTE / oversampling

2. Tuning probability thresholds

3. Gradient boosting models

4. Anomaly detection approaches

5. Cost-sensitive training
