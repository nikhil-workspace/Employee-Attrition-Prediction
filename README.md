# 👥 Employee Attrition Prediction

This project uses machine learning to predict whether an employee is likely to leave an organization (attrition) based on HR data.

---

## 🎯 Objective
Build a classification model to predict employee attrition using demographic, performance, and job-related features.

---

## 📂 Dataset
- Source: [IBM HR Analytics Employee Attrition Dataset (Kaggle)](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- Shape: 1470 rows × 35 columns
- Target: `Attrition` (`Yes`/`No`) → converted to binary (`1` = Yes, `0` = No)

---

## 🔍 Exploratory Data Analysis (EDA)
- Checked class imbalance in `Attrition` (imbalanced: ~84% No, ~16% Yes)
- Visualized correlation with `Attrition`
- Found features like `OverTime`, `JobSatisfaction`, `Age`, and `MonthlyIncome` are important

---

## 🧹 Preprocessing
- Dropped irrelevant columns: `EmployeeNumber`, `Over18`, `StandardHours`, `EmployeeCount`
- Encoded all categorical columns using `LabelEncoder`
- Split data into `X` and `y`, and performed 80-20 train-test split (stratified)

---

## 🤖 Models Used
### 1. Logistic Regression
- Accuracy: ~87%
- ROC AUC: High
- Precision & Recall balanced

### 2. Random Forest Classifier
- Accuracy: ~88%
- Feature importance plotted
- Best performing model overall

---

## 📊 Evaluation Metrics
- Accuracy, Precision, Recall, F1-score
- Confusion Matrix (visual)
- ROC Curve + AUC Score

---

## 📌 Top Predictive Features
- `OverTime`
- `Age`
- `MonthlyIncome`
- `JobLevel`
- `TotalWorkingYears`

---

## 📁 Project Structure
employee-attrition-prediction/
│
├── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── attrition_prediction.ipynb
├── README.md

---

## 💡 Skills Demonstrated
- Data Cleaning & EDA
- Label Encoding & Stratified Split
- Model Training & Evaluation (Logistic Regression, Random Forest)
- Feature Importance Analysis
- ROC-AUC and Classification Metrics

---

## 📌 Note
Due to class imbalance, further improvements can include:
- SMOTE or class_weight balancing
- Trying XGBoost or LightGBM
- Feature selection or dimensionality reduction
