# SALARY-PREDICTION-BY-LINEAR-REGRESSION-
A production-grade Linear Regression solution for transparent salary benchmarking. Implements Ordinal Encoding to preserve the hierarchical nature of Education, with deep diagnostic checks (Residuals vs. Fitted) to validate OLS assumptions. Delivers business metrics, empowering HR teams with data-driven compensation strategies.
# Employee Salary Prediction

A machine learning project that predicts an employee's annual salary based on **Years of Experience** and **Education Level** using Linear Regression.

---

## Objective

To build an interpretable regression model that helps HR teams and businesses determine fair salary benchmarks. The model quantifies exactly how much an extra year of experience or an advanced degree contributes to compensation.

---

## Dataset

The dataset contains employee records with the following key columns:

- `Years of Experience` – Total professional experience (in years)
- `Education Level` – Bachelor's, Master's, or PhD
- `Salary` – Annual salary in USD (Target Variable)

> The dataset includes other fields like `Age`, `Gender`, and `Job Title`, but this project focuses on Experience and Education for simplicity and interpretability.

---

## Tech Stack

- Python 3.8+
- Pandas & NumPy – Data processing
- Matplotlib & Seaborn – Visualization
- Scikit-Learn – Preprocessing, Modeling, Evaluation
- Jupyter Notebook – Interactive development

---

## Methodology

1. **Data Cleaning** – Removed empty rows and fixed malformed salary entries.
2. **EDA** – Visualized relationships to confirm linear trends and education hierarchy.
3. **Feature Engineering** – Applied **Ordinal Encoding** to Education Level:
   - Bachelor's → 0
   - Master's → 1
   - PhD → 2
4. **Model Training** – Used Ordinary Least Squares Linear Regression (80/20 train-test split).
5. **Evaluation** – Measured performance using R², MAE, RMSE, and MAPE.

---

## Results

| Metric | Value |
| :--- | :--- |
| R-squared (R²) | ~0.74 |
| Mean Absolute Error (MAE) | ~$11,200 |
| Average Prediction Accuracy | ~86.5% |

**Interpretation**:  
- Every additional year of experience → ~$5,200 increase in salary.  
- Moving from Bachelor's to Master's → ~$12,000 increase.

---

## How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/employee-salary-prediction.git
   cd employee-salary-prediction
