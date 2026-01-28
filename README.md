# 🏡 House Prices Prediction Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-green)

A **machine learning regression project** that predicts house prices using structured tabular data.  
Multiple models are implemented and compared, including **Lasso Regression**, **Random Forest**, and **Random Forest with hyperparameter tuning**.


> ⚠️ Dataset files (`train.csv`, `test.csv`) are excluded from the repository.

---

## 🎯 Problem Statement

Predict the **final sale price of houses** based on numerical and categorical features such as location, size, quality, and year built.

---

## 🧹 Data Preprocessing

### 🔹 Missing Values
- Features with **>40% missing values** are dropped
- Remaining missing values are handled using:
  - **Median** for numerical features
  - **Mode** for categorical features

### 🔹 Encoding
- Categorical features are encoded using **OneHotEncoder**
- Numerical features are passed through without transformation
- Unknown categories in test data are safely ignored

---

## 🧠 Models Implemented

### 1️⃣ Lasso Regression (Baseline)
- Automatic regularization using **LassoCV**
- 5-fold cross-validation
- Helps reduce overfitting and perform feature selection

---

### 2️⃣ Random Forest Regressor
- Ensemble-based model
- Handles non-linear relationships
- Robust to outliers and feature scaling

---

### 3️⃣ Random Forest + Hyperparameter Tuning
- **RandomizedSearchCV**
- Tuned parameters:
  - `max_depth`
  - `min_samples_leaf`
- Cross-validated using negative MSE

---

## 📊 Evaluation Metric

- Model performance evaluated using **RMSE (Root Mean Squared Error)** on a validation split

---

## 🚀 Prediction & Submission

- Final predictions are generated on the test dataset
- Results are saved in CSV format:
```bash
submission.csv
submission1.csv
