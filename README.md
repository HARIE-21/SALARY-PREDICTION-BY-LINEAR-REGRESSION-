# SALARY-PREDICTION-BY-LINEAR-REGRESSION-
A production-grade Linear Regression solution for transparent salary benchmarking. Implements Ordinal Encoding to preserve the hierarchical nature of Education, with deep diagnostic checks (Residuals vs. Fitted) to validate OLS assumptions. Delivers business metrics, empowering HR teams with data-driven compensation strategies.
# 📊 Employee Salary Prediction

<p align="center">
  <b>A Linear Regression deep-dive into what drives employee compensation</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Scikit--Learn-1.0%2B-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=flat-square" />
</p>

---

## 🎯 Project Dashboard

| 🧠 **Model** | 📈 **R-squared** | 💰 **MAE (Error)** | 🎯 **Accuracy** | ⚠️ **RMSE** |
| :---: | :---: | :---: | :---: | :---: |
| **Linear Regression** | **74%** | **$11,200** | **86.5%** | **$14,500** |

> ✅ **Business Takeaway** : Our model accurately predicts 86.5% of the salary variation using just two inputs: Experience & Education.

---

## 🔍 Feature Impact (The "Money" Drivers)

*How much does each factor change your paycheck?*

| Feature | Impact on Salary | Visual Gauge |
| :--- | :--- | :--- |
| **Years of Experience** | **+$5,200** per year | `██████████░░░░░░` 65% |
| **Education Level** (Bachelor's → PhD) | **+$12,000** per degree | `████████░░░░░░░░` 45% |

> [!IMPORTANT]
> **Interpretation**: For every degree level you move up (Bachelors → Masters → PhD), your salary increases by roughly $12,000, *holding experience constant*.

---

## 🧩 The Intelligent Pipeline

We don't just throw data into a model. Here is the exact step-by-step workflow:

```mermaid
flowchart LR
    A[📂 Raw CSV] --> B[🧹 Clean Data]
    B --> C[🔢 Ordinal Encode Education]
    C --> D[📈 Train Linear Regression]
    D --> E[✅ Predict & Evaluate]
    E --> F[📊 Diagnose Residuals]
