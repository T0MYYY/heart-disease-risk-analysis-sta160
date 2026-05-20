# Heart Disease Risk Factor Analysis — UC Davis STA 160 Midterm Project

<!-- BADGES_BEGIN -->
<p align="center">
  <img alt="Course" src="https://img.shields.io/badge/Course-STA%20160-022851?style=flat-square&labelColor=2a323d">
  <img alt="UC Davis" src="https://img.shields.io/badge/UC%20Davis-Multivariate%20Stats-FFBF00?style=flat-square&labelColor=2a323d">
  <img alt="Term" src="https://img.shields.io/badge/Term-Spring%202023-2a323d?style=flat-square&labelColor=2a323d">
  <img alt="Team" src="https://img.shields.io/badge/Team-Group%20of%204-1f7a3d?style=flat-square&labelColor=2a323d">
  <img alt="Status" src="https://img.shields.io/badge/Status-Midterm-ec5800?style=flat-square&labelColor=2a323d">
  <img alt="Dataset" src="https://img.shields.io/badge/Dataset-CDC%20BRFSS%202015-0194E2?style=flat-square&labelColor=2a323d">
</p>

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3-3776AB?style=flat-square&labelColor=2a323d&logo=python&logoColor=white">
  <img alt="Jupyter" src="https://img.shields.io/badge/Jupyter-notebook-F37626?style=flat-square&labelColor=2a323d&logo=jupyter&logoColor=white">
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-1.x-F7931E?style=flat-square&labelColor=2a323d&logo=scikitlearn&logoColor=white">
  <img alt="statsmodels" src="https://img.shields.io/badge/statsmodels-0.14-3B5C8C?style=flat-square&labelColor=2a323d">
  <img alt="SciPy" src="https://img.shields.io/badge/SciPy-1.x-8CAAE6?style=flat-square&labelColor=2a323d&logo=scipy&logoColor=white">
  <img alt="pandas" src="https://img.shields.io/badge/pandas-2.x-150458?style=flat-square&labelColor=2a323d&logo=pandas&logoColor=white">
  <img alt="seaborn" src="https://img.shields.io/badge/seaborn-0.13-4C72B0?style=flat-square&labelColor=2a323d">
  <img alt="matplotlib" src="https://img.shields.io/badge/matplotlib-3.x-11557C?style=flat-square&labelColor=2a323d&logo=python&logoColor=white">
</p>
<!-- BADGES_END -->

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
