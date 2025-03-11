# 🏦 Credit Risk Prediction Using Machine Learning

## Project Overview
This project aims to predict **credit risk** using **machine learning** techniques. The dataset is highly **imbalanced**, requiring specialized data processing, feature selection, and model tuning to ensure accurate predictions. 

We evaluate different models:
- **Logistic Regression**
- **Random Forest**
- **XGBoost**
- **Neural Network (MLP)**

## Approach & Methodology

### **Data Preprocessing**
- **Handled missing values** using domain-specific imputation strategies.
- **Transformed skewed features** using **log, square root, and cube root** transformations to reduce skewness.
- **Created new features** like **Income Per Person and a Binary Indicator for Late Payments**.
- **Selected optimal features** using **Mutual Information and Correlation Analysis**.

### **Handling Class Imbalance** with different methods
- **Random Forest & Logistic Regression:** class weighting.
- **XGBoost:** scale_pos_weight.
- **Neural Network:** Used **custom loss function (F1 loss)** and **weighted loss** instead of oversampling.

### **Model Training & Hyperparameter Tuning**
- **Used RandomizedSearchCV** for fast and efficient hyperparameter tuning
- **Evaluation Metrics:**  
  - **AUC-ROC (Primary Metric)** to measure model separability.  
  - **F1-Score** to balance precision & recall.
  These Metrics assure a good representation of model performance with Class Imbalance.

### **Model Evaluation & Feature Importance**
- **AUC-ROC curves:** for model comparison.
- **SHAP values:** for feature importance analysis, ensuring model explainability.

---

## **Results & Model Performance**

| Model               | Accuracy | F1 Score | AUC-ROC |
|--------------------|----------|---------|---------|
| Logistic Regression | 0.79     | 0.29    | 0.842    |
| Random Forest      | 0.81     | 0.30    | 0.846    |
| **XGBoost (Best Model)** | **0.78**  | **0.28**  | **0.85**  |
| Neural Network     | 0.85     | 0.34    | 0.76    |

**Best Model: XGBoost** based on AUC-ROC score
- **Highest AUC-ROC (0.85)** → Best classifier for credit risk.