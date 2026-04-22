# Heart Disease Risk Factor Analysis — UC Davis STA 160 Midterm Project

**Course:** STA 160, Spring 2023, UC Davis  
**Team:** Chiyang Chen, Keying Liu, Hanying Xu, Yuze Huang

---

## Dataset

**CDC Behavioral Risk Factor Surveillance System (BRFSS) 2015**

| Property | Value |
|---|---|
| Observations | 253,680 |
| Features | 22 health indicator variables |
| Target variable | `HeartDiseaseorAttack` (binary: 0 / 1) |
| Source | CDC BRFSS 2015 Health Survey |

The dataset includes behavioral and demographic risk factors such as BMI, blood pressure, cholesterol, smoking status, physical activity, diabetes, general health, age, sex, income, and education level.

---

## Analysis Overview

| Section | Description |
|---|---|
| EDA | Data preview, preprocessing (missing value check), and distribution visualizations for all 22 features |
| Contingency Tables & Conditional Entropy | Chi-square contingency tables and conditional entropy H(Y\|X) for each feature vs. the target; odd ratios reported for binary predictors |
| Regression Analysis | Full and reduced logistic regression models; variables pruned by p-value > 0.05 threshold; accuracy reported for both |
| ML Models (KNN, SVM) | K-Nearest Neighbors and Support Vector Machine (sigmoid kernel) classifiers trained and evaluated on the test set |

The entire analysis is performed **twice**:

1. **HD alone** — `HeartDiseaseorAttack` as the binary response variable
2. **HD + Stroke** — a fused binary indicator (`HD_Stroke = HeartDiseaseorAttack | Stroke`) as the response variable, exploring whether adding stroke as a combined outcome changes predictor relationships and model performance

---

## Repository Files

| File | Description |
|---|---|
| `notebook.ipynb` | Main Jupyter notebook with all analysis and outputs |
| `report.pdf` | Written project report |
| `data/heart_disease_health_indicators_BRFSS2015.csv` | BRFSS 2015 dataset (253,680 rows) |

---

## Libraries

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical computation |
| `matplotlib` | Plotting |
| `seaborn` | Statistical visualization |
| `sklearn` | KNN, SVM, train/test split, accuracy scoring |
| `statsmodels` | Logistic regression with p-values |
| `scipy` | Chi-square contingency table tests |
