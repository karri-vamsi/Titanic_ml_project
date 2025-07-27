# 🚢 Titanic Survival Prediction – ML Project

### 📌 Project Overview
This project focuses on predicting passenger survival from the Titanic dataset using advanced machine learning models. The models explored include:
- K-Nearest Neighbors (KNN)
- Bagging with SGDClassifier
- Bagging with Support Vector Classifier (SVC)

The goal is to compare and evaluate the performance of these classifiers after proper data preprocessing and hyperparameter tuning.

---

### 📁 Files
- `Titanic_ML_project.ipynb` — Complete code with preprocessing, modeling, evaluation, and visualization
- `Titanic_full.csv` — Cleaned dataset used for training/testing

---

### 🧠 Workflow Summary

1. **Data Preprocessing**
   - Extracted titles from passenger names
   - Dropped irrelevant columns (`Name`, `Ticket`, `Cabin`, `PassengerId`)
   - Imputed missing age with mean
   - Encoded categorical columns using `OrdinalEncoder` and `OneHotEncoder`
   - Scaled features with `MinMaxScaler`

2. **Models Used**
   - **KNN (with RandomizedSearchCV)**  
     - Best CV Accuracy: ~72%  
     - Test Accuracy: ~74%  
     - Strong at predicting non-survivors

   - **Bagging + SGDClassifier**  
     - Train Accuracy: ~72%  
     - Validation Accuracy: ~71%  
     - Test Accuracy: ~74%  
     - Balanced performance

   - **Bagging + SVC (Tuned)**  
     - Best CV Accuracy: ~70%  
     - Test Accuracy: ~74%  
     - Slightly weaker at predicting survivors

---

### 📊 Model Comparison

| Model                   | CV Accuracy | Test Accuracy | Remarks                              |
| ----------------------- | ----------- | ------------- | ------------------------------------- |
| KNN                     | ~72%        | ~74%          | Strong for class 0 (non-survivors)   |
| Bagging + SGDClassifier | ~71%        | ~74%          | Most balanced and consistent         |
| Bagging + SVC (Tuned)   | ~70%        | ~74%          | Slightly weaker for survivors        |

---

### ✅ Conclusion
All three models gave comparable results. However, the **Bagging + SGDClassifier** model provided the most balanced classification performance between survivors and non-survivors. Proper feature engineering, handling of missing values, and hyperparameter tuning significantly influenced model accuracy.

---

### 📌 Author
**Karri Vamsi**  
Date: July 27, 2025
