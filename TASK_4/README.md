# 🎬 Movie Genre Classification Using Machine Learning

## 📋 Project Overview

This project aims to build a machine learning model that predicts the genre of a movie based on its plot summary or other textual information. Using natural language processing (NLP) techniques such as TF-IDF (Term Frequency-Inverse Document Frequency) for text feature extraction, the model classifies movie genres using popular classifiers including Naive Bayes, Logistic Regression, and Support Vector Machines (SVM).

## 🗃️ Dataset: [IMDb Genre Classification Dataset](https://www.kaggle.com/datasets/hijest/genre-classification-dataset-imdb)

The dataset used in this project contains movie plot summaries and their corresponding genre labels. It consists of multiple files including:

- **description.txt:** Movie IDs with their plot summaries.
- **train_data.txt:** Movie IDs with their genre labels for training.
- **test_data.txt:** Movie summaries for testing.
- **test_data_solution.txt:** True genres for test data to evaluate performance.

The data was loaded and merged by movie ID to associate each plot summary with its corresponding genre label.
---
## 🧰 Tech Stack

- **Python 3:** Primary programming language for development.
- **Pandas:** Data loading, cleaning, and manipulation.
- **NumPy:** Numerical computations and array handling.
- **scikit-learn:** Machine learning library used for:
  - TF-IDF Vectorization (text feature extraction)
  - Classifiers: Naive Bayes, Logistic Regression, Support Vector Machines (LinearSVC)
  - Data splitting, evaluation metrics, and model training.
- **Matplotlib & Seaborn:** Visualization of model performance metrics such as accuracy comparison and confusion matrices.
- **Jupyter Notebook:** Interactive environment used for running and documenting model training, testing, and evaluation.
- **Natural Language Processing (NLP) techniques:** Text preprocessing, including lowercasing, stopword removal, integrated within TF-IDF vectorizer.

---

## 🛠️ Tools and Techniques

- **Data Preprocessing:**
  - Text cleaning, such as lowercasing.
  - Removal of non-numeric movie IDs to clean the dataset.
  
- **Feature Extraction:**
  - TF-IDF vectorizer transforms text summaries to numeric feature vectors, capturing the importance of words within the corpus.

- **Machine Learning Models:**
  - Multinomial Naive Bayes
  - Logistic Regression
  - Support Vector Machines (LinearSVC)
  
- **Evaluation Metrics:**
  - Accuracy
  - F1-Score
  - classification report

- **Model Performance Plot**

---

## 📊 Results

- The models were trained and compared based on accuracy and F1-score.
- LinearSVC was found to be the best performing classifier during validation.
- The model can predict genres of new movie plots, including animation, thriller, drama, etc.


---
## 📝 Author

**Debaswini-M:** [Debaswini-M](https://github.com/Debaswini-M)  






