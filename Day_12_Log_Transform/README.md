# AI-ML Journey - Day 12: Feature Transformation (Log Transform)

## Project Overview
Investigated the impact of Log Transformation on continuous features using the Titanic dataset. The objective was to observe how reducing right-skewness alters the performance of a linear model versus a tree-based model.

## Dataset & Features
* **Source:** Titanic Dataset
* **Predictors ($X$):** `Age` (Continuous, roughly normal) & `Fare` (Continuous, highly right-skewed)
* **Target ($y$):** `Survived` (Binary Classification)

## Core Methodology & Observations

### 1. Baseline Analysis
* **EDA:** PDF and Q-Q plots revealed `Age` was approximately normally distributed, while `Fare` exhibited significant right-skewness.
* **Models Baseline:** Evaluated Logistic Regression and Decision Tree Classifier on untransformed data.

### 2. Log Transformation Implementation
Applied $f(x) = \log(x + 1)$ to both `Age` and `Fare` features.

### 3. Key Findings & Model Behavior
* **Logistic Regression Accuracy:** **Increased.** Linear models assume a linear relationship and are highly sensitive to skewness and outliers. Squeezing the right tail of `Fare` normalized the variance, stabilizing weight updates.
* **Decision Tree Accuracy:** **Unchanged.** Tree-based models split data based on information gain (e.g., Gini impurity or Entropy). Monotonic transformations do not change the relative ordering of values; hence, the exact same split points are chosen.
* **The "Age" Mistake:** Applying a log transform to `Age` (already symmetric/normal) degraded its distribution, introducing left-skewness. *Lesson: Do not blindly apply power transforms to already-normal features.*

## Results Summary
| Model | Pre-Transform Accuracy | Post-Transform Accuracy | Impact |
| :--- | :--- | :--- | :--- |
| **Logistic Regression** | Baseline | Higher | Positive |
| **Decision Tree** | Baseline | Same | Neutral |

## Repository Structure
```text
AI-ML_Journey/
└── Day-12_Log_Transform/
    ├── README.md                      
    ├── Log_Transform.ipynb      
    └── titanic.csv           