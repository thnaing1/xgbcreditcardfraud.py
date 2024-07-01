xgbcreditcardfraud.py

## Credit Card Fraud Detection using eXtreme Gradient Boost (XGBoost)

## Language: Python

## Overview

This project focuses on credit card fraud detection using the eXtreme Gradient Boost (XGBoost) algorithm. The dataset used is the "Credit Card Fraud Detection" dataset from the Free University of Brussels, consisting of European cardholder transactions. The goal is to classify transactions as fraudulent or non-fraudulent in a data stream context.

## Key Concepts

1. **Data Stream Learning**: The dataset is treated as a data stream by chunking it based on the 'Time' feature.
2. **XGBoost Algorithm**: Adapted for batch-based data stream learning to handle concept drift and extreme class imbalance.
3. **Evaluation Metrics**: Average Precision and F1 score are used to assess the model's performance.

## Findings

1. **Performance**: Achieved an Average Precision score of 0.73 and an F1 score of 0.77.
2. **Challenges**: The model might have suboptimal hyperparameters and the batch-based approach may not fully capture complex concept drifts.
3. **Strengths**: The model can handle class imbalance and non-linear relationships in the data effectively.

## Data Collection

The dataset contains transactions made by European cardholders in September 2013, with 492 fraudulent transactions out of 284,807 total transactions.

## Methodology

1. **Data Chunking**: The dataset is divided into chunks based on the 'Time' feature.
2. **Model Training**: The XGBoost model is trained on each chunk iteratively.
3. **Evaluation**: Predictions are made and evaluated for each chunk to track model performance over time.
