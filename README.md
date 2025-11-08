# Fraud Detection System

A machine learning-based fraud detection system for financial transactions using the PaySim dataset. This project implements a hybrid rule-based and ML approach to identify fraudulent transactions with high accuracy.

## Overview

This system analyzes transaction data to detect fraudulent activities using advanced feature engineering, multi-collinearity analysis, and ensemble machine learning models. The hybrid approach combines domain knowledge (transaction type rules) with Random Forest classification to achieve optimal performance on highly imbalanced datasets.

## Features

- **Advanced Feature Engineering**: Cyclical encoding, balance consistency checks, ratio features, and log transformations
- **Multi-collinearity Detection**: VIF-based feature selection to remove redundant features
- **Hybrid Approach**: Rule-based filtering for non-suspicious transaction types combined with ML for suspicious transactions
- **Class Imbalance Handling**: SMOTE oversampling and class weighting techniques
- **Model Optimization**: Hyperparameter tuning using RandomizedSearchCV with stratified cross-validation
- **Comprehensive Evaluation**: ROC-AUC, PR-AUC, confusion matrix, and feature importance analysis

## Dataset

The project uses a PaySim-like fraud dataset with:
- **Rows**: 6.36 million transactions
- **Columns**: 11 features including transaction type, amount, balances, and fraud labels
- **Class Distribution**: Highly imbalanced (~0.13% fraud cases)

### Data Fields
- `step`: Time unit (1-744 hours)
- `type`: Transaction type (PAYMENT, TRANSFER, CASH_OUT, DEBIT, CASH_IN)
- `amount`: Transaction amount
- `nameOrig`: Origin account ID
- `oldbalanceOrg`: Origin account balance before transaction
- `newbalanceOrig`: Origin account balance after transaction
- `nameDest`: Destination account ID
- `oldbalanceDest`: Destination account balance before transaction
- `newbalanceDest`: Destination account balance after transaction
- `isFraud`: Target variable (1=fraud, 0=legitimate)
- `isFlaggedFraud`: System-flagged transactions

## Installation

### Prerequisites
- Python 3.12 or higher
- Virtual environment (recommended)

### Setup

1. Clone the repository or download the project files

2. Create and activate a virtual environment:
python -m venv venv

Windows
venv\Scripts\activate

Linux/Mac
source venv/bin/activate

3. Install dependencies:
pip install -r requirements.txt

```

### Requirements
imbalanced-learn
joblib
numpy
pandas
scikit-learn
statsmodels
```
