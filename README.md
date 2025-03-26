# credit-risk-classification

## Overview of the Analysis

The purpose of this research is to create a credit risk classification model to predict whether a loan is healthy (0) or risky (1). This helps banks and other financial institutions to decide the creditworthiness of their clients and make good lending decisions.

The dataset contains historical lending activity from a peer-to-peer lending services company. The goal is to predict a loan's risk status based on attributes provided in dataset are :
* loan size 
* interest rate 
* borrower income 
* debt to income 
* num of accounts
* derogatory marks
* total debt
* loan status

The target variable in this analysis is `loan_status`, which indicates wherther the loan is healthy loan(0) or high risk loan(1).

#### **Machine Learning Process**  

1. **Data Preprocessing** – Loaded the dataset, separated features (`X`) and target (`y`), and checked for class imbalance.  
2. **Data Splitting** – Divided the dataset into training (75%) and testing (25%) sets.  
3. **Model Training** – Trained a **Logistic Regression** model using the training data.  
4. **Predictions** – Used the trained model to predict loan risk on the test data.  
5. **Evaluation** – Assessed model performance with a **confusion matrix** and **classification report** (accuracy, precision, recall).  

One of the method that used here is *Logistic Regression*:
Logistic regression is a statistical method for predicting binary outcomes from data. It estimates the probability that a loan is high-risk based on financial features.
As preprocess of Logistic Regression, the data will be cleaned and splitting it into subsets for training and testing the model.
Confusion Matrix & Classification Report – Assessed model accuracy, precision, recall, and F1-score to measure how well it classified healthy and high-risk loans.

## Results
 
- **Accuracy:** **99%** – The model correctly predicted loan status in 99% of cases.  
- **Precision:**  
  - **Healthy Loans:** **1.00** (Perfect precision; no false positives).  
  - **High-Risk Loans:** **0.87** (Some healthy loans misclassified as high-risk).  
- **Recall:**  
  - **Healthy Loans:** **1.00** (All healthy loans correctly identified).  
  - **High-Risk Loans:** **0.95** (95% of actual high-risk loans correctly identified).  
- **F1-Score:** **0.91** for high-risk loans (balance between precision and recall).  

## Summary

The **Logistic Regression model** performed **exceptionally well**, achieving **99% accuracy**. It accurately identified **healthy loans (100% recall and precision)** and performed **strongly for high-risk loans (95% recall, 87% precision, and 91% F1-score)**.  

#### **Best Performing Model**  
Since **only one model was used**, Logistic Regression is the best option available. However, its **lower precision (87%) for high-risk loans** suggests some healthy loans were misclassified as high-risk.  

#### **Performance Considerations**  
- If **reducing risk** is the priority, **high recall for high-risk loans (95%)** ensures most risky borrowers are identified.  
- However, a **precision of 87%** means some loans classified as high-risk may actually be healthy, leading to possible missed lending opportunities.  

#### **Recommendation**  
While the model is highly efficient, fine-tuning is necessary to improve accuracy for high-risk loans. Future improvements can include:

Addressing class imbalance (e.g., oversampling high-risk loans using SMOTE).

Experimenting with other models (Random Forest, XGBoost) to benchmark against.

Tuning the classification thresholds to reduce false positives.
