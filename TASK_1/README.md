# Customer Churn Prediction

This project aims to predict customer churn for a subscription-based service using historical customer data. The dataset used is the [Bank Customer Churn Prediction dataset](https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction), which contains information about customers of a bank and whether they have exited the service.

## Objective

The primary objective is to develop a model that can predict whether a customer will churn based on their demographic and account information. This can help businesses take proactive measures to retain customers.

## Dataset 

The dataset consists of 14 columns:

- **CustomerId**: Unique identifier for each customer
- **Surname**: Last name of the customer
- **CreditScore**: Credit score of the customer
- **Geography**: Country of the customer (e.g., France, Spain, Germany)
- **Gender**: Gender of the customer
- **Age**: Age of the customer
- **Tenure**: Number of years the customer has been with the bank
- **Balance**: Account balance of the customer
- **NumOfProducts**: Number of products the customer has with the bank
- **HasCrCard**: Whether the customer has a credit card (1 = Yes, 0 = No)
- **IsActiveMember**: Whether the customer is an active member (1 = Yes, 0 = No)
- **EstimatedSalary**: Estimated salary of the customer
- **Exited**: Whether the customer has exited the bank (1 = Yes, 0 = No)

## Approach

1. **Data Preprocessing**:
   - Load and inspect the dataset
   - Handle missing values
   - Drop irrelevant columns (`CustomerId`, `Surname`, `RowNumber`)
   - Encode categorical features (`Geography`, `Gender`)
   - Standardize numerical features

2. **Model Development**:
   - Split the data into training and testing sets
   - Train multiple models:
     - Logistic Regression
     - Random Forest Classifier
     - Gradient Boosting Classifier

3. **Model Evaluation**:
   - Evaluate models using accuracy, F1 score, and classification reports
   - Compare model performance using bar charts
   - Plot ROC-AUC curves for each model
   - Display confusion matrices

4. **Feature Importance**:
   - Analyze feature importance using the Gradient Boosting model
     
---

## Tech Stack :

  The project uses the following technologies and libraries:

- **Programming Language:** Python 3.x  
- **Data Manipulation:** pandas, numpy  
- **Data Preprocessing & Encoding:** scikit-learn (`StandardScaler`, `OneHotEncoder`, `OrdinalEncoder`, `ColumnTransformer`)  
- **Machine Learning Models:**  
  - Logistic Regression  
  - Random Forest Classifier  
  - Gradient Boosting Classifier  
- **Model Evaluation:** scikit-learn (`accuracy_score`, `f1_score`, `classification_report`, `roc_curve`, `auc`, `confusion_matrix`)  
- **Data Visualization:** matplotlib, seaborn (for plots like feature importance, model performance, ROC curves, and confusion matrices)

---
## Author:
`Debaswini`
---
