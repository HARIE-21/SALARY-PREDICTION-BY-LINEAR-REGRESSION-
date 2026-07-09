# SALARY-PREDICTION-BY-LINEAR-REGRESSION-
A production-grade Linear Regression solution for transparent salary benchmarking. Implements Ordinal Encoding to preserve the hierarchical nature of Education, with deep diagnostic checks (Residuals vs. Fitted) to validate OLS assumptions. Delivers business metrics, empowering HR teams with data-driven compensation strategies.
# 💰 Employee Salary Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue.svgblue.svg)
![Sc)
![Scikit-Learn](https://imgikit-Learn](https://img.shields.io/badge.shields.io/badge/Scikit--Learn-1./Scikit--Learn-1.0+-orange0+-orange.svg)
![License](https://img.svg)
![License](https://img.shields.io/badge.shields.io/badge/License-MIT-green.svg/License-MIT-green.svg)
![Jupyter]()
![Jupyter](https://img.shields.io/badge/Jhttps://img.shields.io/badge/Jupyter-Notupyter-Notebook-redebook-red.svg)

A.svg)

A comprehensive machine comprehensive machine learning project that learning project that predicts employee predicts employee salaries based salaries based on **Years on **Years of Experience** and of Experience** and **Education Level** using Linear **Education Level** using Linear Regression. This Regression. This project includes detailed project includes detailed Explor Exploratory Dataatory Data Analysis (EDA), feature engineering Analysis (EDA), feature engineering, model diagnostics, model diagnostics,, and business-ready evaluation and business-ready evaluation metrics.

## metrics.

## 📌 Table of 📌 Table of Contents
- Contents
- [Project Overview](#-project-overview [Project Overview](#-)
- [Datasetproject-overview)
- [Dataset](#-dataset)
-](#-dataset)
- [Tech [Tech Stack](# Stack](#-tech-stack)
- [Method-tech-stackology](#-)
- [Methodology](#-methodology)
- [Keymethodology)
- Results](#-key [Key Results](#-key-results)
--results)
- [Model Diagnostics [Model Diagnostics](#-model-diagnostics)
-](#-model-diagnostics)
- [Limitations & Future Work [Limitations &](#-limitations Future Work](#-limitations--future-work--future-work)
- [Install)
- [Installation & Usageation & Usage](#-installation--](#-installation--usage)
-usage)
- [Contributing](# [Contributing](#-contributing-contributing)

---

##)

---

## 📖 Project Overview 📖

The goal Project Overview

The goal of this project of this project is to build a robust is to build a robust regression model that regression model that helps HR helps HR departments and departments and businesses determine businesses determine fair fair salary benchmarks salary benchmarks.. 

While many factors influence 

While many factors compensation influence compensation, this, this project project focuses on two focuses on two fundamental fundamental drivers drivers: **professional experience** and **: **professionaleducational attainment**. The experience** and **educational attainment**. The model provides interpret model provides interpretable coefficientsable coefficients, allowing, allowing stakeholders stakeholders to quantify to quantify exactly exactly how much an extra how year of experience or much an extra an advanced degree contributes year of experience or an advanced degree contributes to salary to salary.

>.

> **Business **Business Value**: Red Valueuces bias**: Reduces bias in compensation in compensation discussions discussions and provides data-backed and provides data-backed justification justification for salary for salary negotiations negotiations.

---

##.

---

## 📊 Dataset

The 📊 Dataset

The dataset (` dataset (`Salary DataSalary Data.csv`) contains synthetic.csv`) contains synthetic employee employee records with the following features records with:

| Column | the following features Type | Description |
|:

| Column | Type | Description |
| :--- | : :--- | :--- | :------ | :--- |
| `Age |
| `Age` | Integer | Employee's age |
|` | Integer | Employee `Gender` |'s age |
| `Gender` | Categorical | Categorical | Male / Male / Female |
| ` Female |
| `Education Level` |Education Level` | Categorical | Bachelor Categorical | Bachelor's, Master's's, Master's, PhD |
|, PhD |
| `Job Title `Job Title` | Categorical` | Categorical | Specific | Specific role (e.g., role ( Software Engineer) |
|e.g., Software Engineer) |
| `Years of Experience `Years of Experience` |` | Integer Integer | Total | Total professional professional experience in years experience in years |
| `Salary |
| `Salary` | Integer` | Integer | Annual | Annual salary in USD *( salary in USD *(Target VariableTarget Variable)* |

**Note**: While the)* |

**Note raw**: While the raw data includes ` data includes `Job Title` andJob Title` and `Gender`, this `Gender`, this iteration iteration uses uses **Years **Years of Experience** and **Education Level** of Experience** and **Education Level** as predictive features to maintain as predictive model features to maintain simplicity and interpret model simplicity and interpretability.

---

##ability.

---

## 🛠️ 🛠️ Tech Stack

- Tech Stack

- **Language **Language**: Python **: Python 3.83.8+
- **L+
- **Libraries**:
  - `ibraries**Pandas` &:
  - `Pandas` & `NumPy` - `NumPy` - Data manipulation Data manipulation
  - `Mat
  - `Matplotlib` & `plotlib` & `Seaborn`Seaborn` - Data visualization - Data visualization
  - `Sc
  - `Scikit-Learnikit-Learn` - Preprocessing, Modeling` - Pre, and Evaluationprocessing, Modeling
- **Environment, and Evaluation
- **Environment**: Jupyter Notebook**: Jupyter Notebook / VS Code

---

## / VS Code

---

## 🔬 Methodology

### 🔬 Methodology

### 1. Data 1. Data Cleaning
- Removed empty rows Cleaning
- Removed empty rows and mal and malformed entriesformed entries (e.g., a salary (e value.g., a salary value of `350` of `350` instead instead of `35000`).
- Converted `Salary` to a numeric type, coercing errors of `35000`).
- Converted `Salary` to a numeric type, coercing errors to `NaN to `NaN` for safe dropping.

### 2. Exploratory Data Analysis (EDA)
- **` for safe dropping.

### 2. Exploratory Data Analysis (EDA)
- **Distribution Check**: VerifiedDistribution Check**: Verified that salary is normally distributed with a right-sk that salary is normally distributed with a right-skew (high-earning executives).
- **Relationship Analysis**: Scew (high-earning executives).
- **Relationship Analysis**: Scatter plots confirmedatter plots confirmed a strong positive linear correlation between Years a strong positive linear correlation between Years of Experience and Salary.
- **Categorical Trends**: Box plots of Experience and Salary.
- **Categorical Trends**: Box plots revealed a clear hierarchy—Ph revealed a clear hierarchy—PhDs earn significantly more than MasterDs earn's, who significantly more than Master earn more than Bachelor's.

###'s, who earn more than Bachelor's.

### 3. Feature 3. Feature Engineering (Crucial Decision Engineering (Crucial Decision)
Instead)
Instead of using One-Hot Encoding of using One-Hot Encoding (which would (which would treat education treat education levels as independent levels as independent categories), I categories), I applied **Ordinal Encoding**:

- applied **Ordinal Encoding**:

- ` `Bachelor's` →Bachelor's` → `0 `0`
- `Master's``
- `Master's` → `1 → `1`
- `PhD` → `2`
- `PhD` → `2`

**Why?`

**Why?** Linear Regression assumes a numeric** Linear relationship Regression assumes a numeric relationship. Ordinal encoding. Ordinal encoding preserves the logical preserves the logical ranking of education, allowing the model ranking of to calculate a education, allowing the model to calculate a single "bump" single "bump" in salary in salary per degree level per degree level, which is, which is more interpret more interpretable and statistically efficientable and statistically efficient.

### 4..

### 4. Model Training Model Training
- **Algorithm
- **Algorithm**: Ordinary**: Ordinary Least Squares (OLS) Least Squares (OLS) Linear Regression.
- **Optimization**: Sc Linear Regression.
- **Optimization**: Scikit-Learn’s implementation uses Singularikit-Learn’s implementation uses Singular Value Decomposition (SVD) for stable coefficient calculation.
- **Split**:  Value Decomposition (SVD) for stable coefficient calculation.
- **Split**: 80% training / 20% testing (`random_state=4280% training / 20% testing (`random_state=42` for reproducibility).

### 5. Evaluation
- **R` for reproducibility).

### 5. Evaluation
- **R² (Coefficient of Determination)² (Coefficient of Determination)**: Measures the proportion of variance explained by the model.
- **MAE (Mean Absolute Error)**:**: Measures the proportion of variance explained by the model.
- **MAE (Mean Absolute Error)**: Average Average dollar dollar amount the amount prediction the prediction is off by is off by.
- **RMSE (Root Mean Square Error)**: Penalizes large outliers (e.
- **RMSE (Root Mean Square Error)**: Penalizes large outliers (e.g., CEO salaries).
- **MAPE (Mean Absolute Percentage Error)**:.g., CEO salaries).
- **MAPE (Mean Absolute Percentage Error)**: Converted into a business-friendly " Converted into a business-friendly "Accuracy PercentageAccuracy Percentage".

---

## 📈 Key Results

| Metric | Score |
| :--- |".

---

## 📈 Key Results

| Metric | Score |
| :--- | :--- |
| :--- |
| **R-squared **R-squared ( (R²)** |R²)** | ~ 0 ~ 0.74 (74% of variance.74 (74% of variance explained) |
| explained) |
| **Mean Absolute Error **Mean Absolute Error (MAE)** (MAE)** | ~ $ | ~ $11,20011,200 |
| **Root Mean Squared Error |
| **Root (RMSE)** | ~ $14 Mean Squared Error (RMSE)** | ~ $14,500,500 |
| **MAP |
| **MAPE AccuracyE Accuracy** | ~ ** | ~ 8686.5%.5% |

> **Interpretation**: |

> **Interpretation**: The model correctly predicts The model correctly predicts a a given given employee's salary within 86 employee's salary within 86.5% accuracy.5% accuracy on average. For every additional on average. For every year of experience, additional salary increases by approximately **$5 year of experience, salary increases by approximately **$5,200**, and,200**, and moving from a Bachelor's to a moving from a Bachelor's to a Master's yields Master's yields an average increase of ** an average increase of **$12,000$12,000**.

---

## 🔍 Model Diagnostics**.

---

## 🔍 Model Diagnostics

### Residual

### Residuals vs. Predicted Plot
As vs. Predicted Plot
A critical diagnostic to validate critical diagnostic to validate the assumptions of Linear Regression the assumptions of Linear Regression.

![Residuals Plot](images/residuals_plot.png).

![Residuals Plot](images/residuals_plot.png) *(Replace with your actual plot path)*

- **What it checks**: *(Replace with your actual plot path)*

- **What it checks**: The plot ensures the errors The plot ensures the errors (residuals) are randomly distributed around zero.
- ** (residuals) are randomly distributed around zero.
- **Finding**: InitialFinding**: Initial results showed slight heteroscedasticity (widening funnel results showed slight heteroscedasticity (widening funnel at higher salaries), indicating that high-level at higher salaries), indicating that high-level executives have more executives have more variance not captured by experience/education alone variance not captured by experience/education alone.
- **Action**: This validated the decision to eventually add more.
- **Action**: This validated the decision to eventually add more features (like Job Title) in future versions.

---

## features (like Job Title) in future versions.

---

## ⚠️ Limitations & Future Work

### Limitations
- **Missing "Skills" Column ⚠️ Limitations & Future Work

### Limitations
- **Missing "Skills" Column**: The prompt**: The prompt aimed to aimed to include include Skills, but the raw data lacks Skills, but the raw data lacks this feature this feature. Hard. Hard skills (e.g., Python skills (e.g., Python, SQL) significantly, SQL) significantly impact salary and impact salary and are are missed here missed here.
- **Linear.
- **Linear Assumption**: Assumption**: The The model assumes a model assumes a straight-line relationship; straight-line relationship; diminishing diminishing returns on experience may returns on experience may require polynomial require polynomial terms.
- ** terms.
- **Limited FeaturesLimited Features**: Factors**: Factors like company like company size, geographic location, and industry size, geographic location, and industry are absent are absent.

### Future Work.

### Future Work (Roadmap)
1. (Roadmap)
1.  **Pol  **Polynomial Features**: Add `ynomial Features**: Add `Experience^2` to captureExperience^2` to capture the diminishing salary the diminishing salary growth growth over time over time.
2. .
2.  **Skill Extraction **Skill Extraction**: Scrape job**: Scrape job descriptions to create binary features descriptions to create binary features for specific technical skills.
3.  **Regularization**: Implement Ridge/Lasso regression to prevent for specific technical skills.
3.  **Regularization**: Implement Ridge/Lasso regression to prevent overfitting if we add hundreds of skill columns overfitting if we add hundreds of skill columns.
4. .
4.  **Tree-Based Models**: Test Random **Tree-Based Models**: Test Random Forest or Forest or XGBoost XGBoost to see if non-linear interactions to see if non-linear interactions improve the R² score improve the R² score.

---

##.

---

## 🚀 Installation & Usage

To run this project locally:

1. **Clone the 🚀 Installation & Usage

To run this project locally:

1. **Clone the repository**
   ```bash
   git clone https://github.com/your- repository**
   ```bash
   git clone https://github.com/your-username/employee-salary-prediction.git
   cd employee-salary-prediction
  username/employee-salary-prediction.git
   cd employee-salary-prediction
