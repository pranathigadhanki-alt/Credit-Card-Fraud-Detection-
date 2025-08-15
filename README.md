Credit Card Fraud Detection – Exploratory Analysis
Project Overview

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

Identified transactions above the 99th percentile of the Amount feature as potentially suspicious.

Compared descriptive statistics of the Amount feature between fraudulent and non-fraudulent transactions.

Data Visualization

Created histograms with KDE plots for the Amount variable, separated by fraud and non-fraud classes.

Highlighted differences in the amount distribution between the two transaction types.

Key Results

Dataset Size: 284,807 transactions × 31 columns.

Class Distribution:

Non-fraud: 284,315 transactions

Fraud: 492 transactions (~0.1727%)

99th Percentile Transaction Amount: Approximately $1,017.97.

Amount Summary (Median / Mean / Max):

Non-fraud: Median = $22.00, Mean = $88.29, Max = $25,691.16

Fraud: Median = $9.25, Mean = $122.21, Max = $2,125.87

Fraudulent transactions often involve smaller amounts than non-fraudulent transactions, though high-value fraudulent cases do exist.

Insights

The analysis confirmed the dataset’s extreme class imbalance and revealed distinct patterns in transaction amounts for fraudulent vs. non-fraudulent transactions. Fraudulent transactions tend to cluster at lower amounts, but the presence of large fraudulent transactions suggests that high-value monitoring is still important.
