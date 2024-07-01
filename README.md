xgbcreditcardfraud.py

## Credit Card Fraud Detection using eXtreme Gradient Boost (XGBoost)

## Language: Python

## Abstract

Credit card fraud has become a growing problem with the rise of online banking. Customers and financial institutions alike face rising financial costs. With this problem emerges new ways of tackling credit card fraud. This study includes one of the ways to tackle one aspect of the credit card fraud detection problem. Credit card fraud detection is a data stream problem, an incremental learning problem, that is fundamentally different from a static learning problem. The problem includes dealing with class imbalance as well as concept drift. Traditional ways of dealing with credit card fraud include rule check-based systems. Such rules are often determined based on statistical analysis of historical data. However, the emergence of machine learning-based methods promises to improve the accuracy of credit card fraud detection. The goal is to not only reduce false alarms but also to detect more true frauds in any data stream. My method is based on eXtreme Gradient Boost which is adapted to work with data streams. It is an ensemble decision tree-based machine-learning algorithm. Instead of using the entire dataset as input, it is capable of using smaller chunks or batches of the incoming data stream. The model is tested using Average Precision and F1 score on 24 chunks of data with each chunk of data representing 2 hours of the stream. The testing reveals an Average Precision score of 0.73 and an F1 score of 0.77. This is a good score, but not an amazing score. My model can achieve good precision across different recall levels and maintains a good balance between precision and recall.

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
