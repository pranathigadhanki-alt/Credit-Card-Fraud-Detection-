# Credit Card Fraud Detection – Exploratory Analysis

## Project Overview  
- **Description:** This project performs an exploratory analysis of the Credit Card Fraud Detection dataset from Kaggle, focusing on understanding the dataset structure, identifying suspicious transaction patterns, and visualizing trends in transaction amounts.  
- **Goal:** Build foundational understanding and insights before developing any machine learning models.  
- **Implementation:** Google Colab  
- **Level:** Beginner (no predictive modeling)

## Dataset Description  
- **Total transactions:** 284,807  
- **Features:** 30 PCA-transformed variables (V1–V28), `Time`, `Amount`, and `Class`  
- **Target variable:** `Class` (0 = non-fraud, 1 = fraud)  
- **Class imbalance:** Fraudulent transactions make up ~0.1727% of the total  

## Methods and Workflow  
- **Data Loading and Exploration:**  
  - **Step 1:** Imported the dataset into pandas  
  - **Step 2:** Displayed the first five rows  
  - **Step 3:** Generated descriptive statistics  
  - **Step 4:** Checked data types and null values  
  - **Step 5:** Counted fraud vs. non-fraud cases  

- **Suspicious Pattern Detection:**  
  - **Step 1:** Flagged transactions above the 99th percentile in `Amount`  
  - **Step 2:** Compared `Amount` statistics between fraud and non-fraud classes  

- **Data Visualization:**  
  - **Step 1:** Created KDE histograms of transaction amounts  
  - **Step 2:** Visually compared class-wise distribution differences  

## Key Results  
- **Dataset size:** 284,807 transactions × 31 columns  
- **Class distribution:** 284,315 non-fraud vs. 492 fraud cases (~0.1727% fraud rate)  
- **99th percentile transaction amount:** approximately 1,017.97  
- **Median amount:**  
  - **Non-fraudulent:** 22.00  
  - **Fraudulent:** 9.25  
- **Mean amount:**  
  - **Non-fraudulent:** 88.29  
  - **Fraudulent:** 122.21  
- **Maximum amounts:**  
  - **Non-fraudulent:** 25,691.16  
  - **Fraudulent:** 2,125.87  

## Insights  
- **Insight 1:** Fraudulent transactions often involve smaller amounts than non-fraudulent ones, though large-value fraud still occurs  
- **Insight 2:** Class imbalance is extreme and must be addressed in modeling  
- **Insight 3:** Precision, recall, and PR-AUC are more appropriate metrics than accuracy  
