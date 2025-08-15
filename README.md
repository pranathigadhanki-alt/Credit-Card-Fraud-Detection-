Credit Card Fraud Detection – Exploratory Analysis Project Overview

This project performs an exploratory analysis of the Credit Card Fraud Detection dataset from Kaggle, focusing on understanding the dataset structure, identifying suspicious transaction patterns, and visualizing trends in transaction amounts. The goal is to build foundational understanding and insights before developing any machine learning models. The analysis is implemented in Google Colab and is designed for a beginner-level workflow without predictive modeling.

Dataset Description

The dataset contains 284,807 transactions made by European cardholders in September 2013. Each transaction is represented by 30 numerical input variables, most of which are the result of a PCA transformation (V1–V28), along with the original Time and Amount features, and the target variable Class:

Class = 0 → Non-fraudulent transaction

Class = 1 → Fraudulent transaction

The dataset is highly imbalanced, with fraudulent transactions making up only 0.1727% of the total.

Methods and Workflow

The analysis was divided into three main steps:

Data Loading and Exploration

Imported the dataset into pandas.

Displayed the first five rows for initial inspection.

Generated descriptive statistics to understand data ranges and distributions.

Used info() to check data types and null values.

Counted occurrences of fraudulent and non-fraudulent transactions to confirm class imbalance.

Suspicious Pattern Detection

Identified transactions with amounts greater than the 99th percentile as potentially suspicious.

Compared the amount distributions between fraudulent and non-fraudulent transactions.

Data Visualization

Created histograms for transaction amounts, separated by fraud and non-fraud classes, to visually compare distributions.

Key Results

Dataset size: 284,807 transactions × 31 columns.

Class distribution: 284,315 non-fraud vs. 492 fraud cases (~0.1727% fraud rate).

99th percentile transaction amount: approximately 1,017.97.

Median amount:

Non-fraudulent transactions: 22.00

Fraudulent transactions: 9.25

Mean amount:

Non-fraudulent transactions: 88.29

Fraudulent transactions: 122.21

Maximum amounts:

Non-fraudulent: 25,691.16

Fraudulent: 2,125.87

Insights

Fraudulent transactions often involve smaller amounts than non-fraudulent transactions, although there are notable cases of high-value fraud. The dataset’s extreme class imbalance highlights the importance of using precision and recall over accuracy in future predictive modeling.
