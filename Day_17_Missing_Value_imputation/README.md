# Day 17: Feature Engineering - Missing Value Imputation & Covariance Distortion

## Project Overview
This repository explores the statistical consequences of **Univariate Missing Value Imputation** (Mean/Median) using the Titanic dataset. Beyond simply filling missing entries, this analysis mathematically tracks how imputation distorts data distribution, variance, covariance, and outlier detection frameworks.

## Key Statistical Insights

### 1. The Variance Compression Proof
By analyzing the covariance matrix diagonal, we observe an explicit artificial compression of variance when constants are introduced:
* **Original Age Variance:** 210.25
* **Mean Imputed Age Variance:** 168.85 (~20% reduction)
* **Median Imputed Age Variance:** 169.20 (~19.5% reduction)

*Note on Covariance Behavior:* Calculating covariance between the original `Age` column and imputed columns returns identical values ($210.25$) due to pairwise row deletion (`dropna`) during computation, masking the underlying variance shrinkage happening on the diagonal.

### 2. Box Plot & Outlier Mechanics
Imputing central tendencies (mean/median) drastically compresses the Interquartile Range (IQR). As a result:
* The distribution gets narrower.
* The standard box plot whiskers contract.
* Normal peripheral data points are artificially flagged as "outliers" purely due to the shrunken IQR bounds.

## Automation Pipeline
Transitioned from manual Pandas execution to an enterprise-grade, reproducible workflow utilizing scikit-learn's `SimpleImputer` and `ColumnTransformer`.

---

## Repository Structure
```text
AI-ML_Journey/
└── Day_17_Missing_Value_Imputation/
    ├── README.md
    ├── day_17_missing_value_imputation.ipynb
    └── titanic_toy.csv