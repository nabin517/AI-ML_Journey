# AI-ML Journey: Day 19 - Feature Engineering

## Overview
Day 19 focuses on maximizing model performance through **Feature Construction** and **Feature Splitting** using the Titanic dataset. By transforming raw variables into domain-specific features, the baseline cross-validation accuracy improved from **69% to 70%**.

## Feature Engineering Strategies

### 1. Feature Construction (`Family_size` & `Family_type`)
Combined interacting features (`SibSp` and `Parch`) into a single, cohesive metric to capture social dynamics on the Titanic.
* **`Family_size`**: Calculated as `SibSp + Parch + 1` (including the passenger).
* **`Family_type`**: Categorized based on size thresholds:
  * `0`: Alone (`Family_size == 1`)
  * `1`: Small Family (`1 < Family_size <= 4`)
  * `2`: Large Family (`Family_size > 4`)

### 2. Feature Splitting (`Title` & `Is_Married`)
Isolated high-cardinality data from the `Name` column to extract hidden demographic signals.
* **`Title`**: Extracted salutations (e.g., Mr, Mrs, Miss, Master).
* **`Is_Married`**: A binary flag (`1` for married, `0` otherwise) explicitly mapped from the `Mrs` title to capture socioeconomic survival bias.

## Results
* **Baseline Cross-Validation Score:** 69%
* **Post-Feature Engineering Cross-Validation Score:** 70% (+1% absolute improvement)

---

## Repository Structure

```text
├── data/
│   └── titanic.csv               # Raw dataset
├── notebooks/
│   └── day_19_feature_eng.ipynb  # Main implementation notebook
├── README.md                     # Project documentation