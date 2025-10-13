# 💳 CREDIT CARD FRAUD DETECTION

A machine learning project aimed at detecting fraudulent credit card transactions using supervised learning techniques.  
This project explores multiple models — **Logistic Regression**, **Decision Tree**, and **Random Forest** — to classify whether a transaction is **fraudulent** or **legitimate**.

---

## 📘 Project Description

Credit card fraud is a significant concern in the financial system. With millions of daily transactions, efficiently identifying fraud is crucial to minimizing financial losses and protecting customers.

This project builds a classification model using historical transaction data to predict whether a given transaction is fraudulent.  
The dataset contains both **training** and **testing** transaction records, which are cleaned, preprocessed, and used to train and evaluate multiple machine learning models.

---

## 📊 Dataset Information

**Source:** [Kaggle – Fraud Detection Dataset](https://www.kaggle.com/datasets/kartik2112/fraud-detection)

The dataset consists of two CSV files:
- `fraudTrain.csv`
- `fraudTest.csv`

Each file contains anonymized transaction records with details such as:
- Transaction amount  
- Merchant and category information  
- Cardholder’s demographic details (e.g., job, gender, DOB)  
- Target variable: **`is_fraud`** (1 = Fraudulent, 0 = Legitimate)

---

## ⚙️ Technologies and Libraries Used

- **Python** 
- **Pandas** – Data handling and preprocessing  
- **NumPy** – Numerical operations  
- **Scikit-learn** – Machine learning, metrics, and preprocessing  
- **Imbalanced-learn (SMOTE)** – Balancing the dataset  
- **Matplotlib** – Data visualization and performance plots  

---

## 🧩 Project Workflow

### 1. **Data Loading**
Both `fraudTrain.csv` and `fraudTest.csv` are loaded using Pandas and concatenated for unified preprocessing.

### 2. **Data Cleaning and Feature Engineering**
- Removed irrelevant and personal columns like names, city, latitude, longitude, etc., to reduce noise and protect PII.
- Created a new feature **`age`** by calculating from the `dob` (date of birth) column.
- Dropped `dob` after extraction.
- Checked unique values in categorical features such as `job` and `category`.

### 3. **Feature Encoding and Scaling**
Used a `ColumnTransformer` for preprocessing:
- **OneHotEncoder** for categorical columns (`category`, `job`)
- **OrdinalEncoder** for binary feature (`gender`)
- **StandardScaler** for numerical features (`amt`, `age`)

### 4. **Data Splitting**
Split the dataset into:
- **70% training set**
- **30% testing set**  
(Stratified by `is_fraud` to maintain class ratio)

### 5. **Handling Class Imbalance**
Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the training dataset since the fraud class was heavily underrepresented.

### 6. **Model Training**
Trained and compared three models:
- **Logistic Regression**  
- **Decision Tree Classifier**  
- **Random Forest Classifier**

Each model was trained using balanced data and tested on the original test set.

### 7. **Model Evaluation**
Evaluated models using:
- **Accuracy**
- **F1 Score (binary)**
- **Classification Report**
- **ROC-AUC Curve**
- **Confusion Matrix**

A custom function was created to evaluate and print metrics for each model.

---

## 🧠 Model Performance Summary

| Model                | Accuracy | F1 Score |
|----------------------|:--------:|:--------:|
| Logistic Regression  | 0.8911   | 0.0699   |
| Decision Tree        | 0.9565   | 0.1869   |
| Random Forest        | 0.9784   | 0.2673   |


---

## 📈 Visualizations

The notebook includes multiple visualizations:
- **Model Comparison Bar Chart** – compares Accuracy and F1 score across models  
- **ROC AUC Curve** – visual comparison of models’ performance  
- **Confusion Matrix** – visualization of Decision Tree performance  
- **Fraud Probability Check** – predicted probabilities for actual fraud cases  

---

## 🧾 Key Insights

- Fraudulent transactions form a very small portion of the dataset, making the classification problem **highly imbalanced**.  
- **SMOTE** effectively helped balance the training data and improved F1 scores.  
- **Random Forest** performed best due to its ensemble nature and ability to capture complex relationships.  
- **Accuracy alone is misleading** — F1 and ROC-AUC are more suitable metrics for this problem.

---

## Author
`Debaswini`
---
