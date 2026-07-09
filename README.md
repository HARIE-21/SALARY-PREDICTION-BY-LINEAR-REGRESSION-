# SALARY-PREDICTION-BY-LINEAR-REGRESSION-
A production-grade Linear Regression solution for transparent salary benchmarking. Implements Ordinal Encoding to preserve the hierarchical nature of Education, with deep diagnostic checks (Residuals vs. Fitted) to validate OLS assumptions. Delivers business metrics, empowering HR teams with data-driven compensation strategies.
# 👨‍💼 Employee Attrition Prediction

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0+-orange.svg)](https://scikit-learn.org/)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> **Predicting employee churn using Logistic Regression to help HR teams proactively retain top talent.**

---

## 📌 Overview

Employee turnover is costly. This project builds a **machine learning pipeline** that predicts whether an employee is likely to leave the company based on HR data (e.g., salary, overtime, job satisfaction, and work-life balance).

The solution focuses on:
- **Interpretability**: Logistic Regression provides clear, business-friendly coefficients.
- **Production-readiness**: A `Pipeline` with `ColumnTransformer` ensures zero data leakage.
- **Actionable insights**: Identifies the top drivers of attrition (e.g., Overtime, Monthly Income, Job Satisfaction).

---

## 📊 Dataset

The dataset (`test.csv`) contains **~10,000 employee records** with the following features:

| Type | Features |
| :--- | :--- |
| **Numerical** | Age, Monthly Income, Years at Company, Number of Promotions, Distance from Home, Company Tenure, Number of Dependents |
| **Categorical** | Gender, Job Role, Job Satisfaction, Work-Life Balance, Overtime, Education Level, Marital Status, Remote Work, etc. |
| **Target** | `Attrition` (Left / Stayed) |

---

## 📁 Project Structure

```text
employee-attrition-prediction/
│
├── data/
│   └── test.csv                 # Raw dataset
│
├── notebooks/
│   └── employee_attrition.ipynb # Full Jupyter Notebook (code + explanations)
│
├── src/                         # (Optional) Python scripts
│   └── predict.py               
│
├── requirements.txt             # Python dependencies
└── README.md                    # You are here!
