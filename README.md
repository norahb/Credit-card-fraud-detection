# Credit Card Fraud Detection

## Overview

This project implements a machine learning model for detecting fraudulent credit card transactions. The model is designed to handle highly imbalanced datasets, using techniques such as SMOTE (Synthetic Minority Over-sampling Technique) and Random Forest classification. The goal is to accurately identify fraudulent transactions while minimizing false positives.

## Dataset

The dataset used in this project contains transactions made by credit cards in September 2013 by European cardholders. It includes:

- **Total Transactions**: 284,807
- **Fraudulent Transactions**: 492 (0.172% of all transactions)

### Features

- The dataset contains only numerical input variables, which are the result of PCA (Principal Component Analysis) transformation. 
- Features V1, V2, ..., V28 are the principal components obtained with PCA.
- **Time**: Seconds elapsed between each transaction and the first transaction in the dataset.
- **Amount**: The transaction amount.
- **Class**: The response variable (1 for fraud, 0 for legitimate transactions).

Due to confidentiality issues, the original features are not provided.

## Model Performance

After training the model, the following performance metrics were obtained:

- **AUC-ROC Score**: 0.9760
- **Classification Report**:
    ```
                  precision    recall  f1-score   support

               0       1.00      1.00      1.00     56864
               1       0.70      0.89      0.78        98

        accuracy                           1.00     56962
       macro avg       0.85      0.94      0.89     56962
    weighted avg       1.00      1.00      1.00     56962
    ```

## Installation

To run this project, you'll need to have Python installed along with the following libraries:

```bash
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn