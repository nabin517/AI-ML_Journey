# Day 16: Complete Case Analysis (CCA)

## Overview
Day 16 focuses on handling missing data by removing incomplete records, specifically using Complete Case Analysis (CCA), also known as listwise deletion. This method involves discarding any rows that contain one or more missing values.

## Theoretical Foundations
CCA is a valid strategy only when specific assumptions are met. Applying it blindly can introduce severe bias and reduce the statistical power of the model.

### Assumptions for CCA
* **Missing Completely at Random (MCAR):** The probability of a value being missing is completely independent of any observed or unobserved data. The missingness is entirely random.
* **Missing Threshold (< 5%):** Typically, CCA is only acceptable if the total missing data across the target columns constitutes less than 5% of the entire dataset. This ensures that dropping rows does not result in an unacceptable loss of information.

### Risks of Violation
* If data is not MCAR, dropping rows introduces systematic bias.
* If missingness exceeds 5%, a significant portion of the training data is wasted, which can degrade model performance.

---

## Dataset Analysis & Implementation

### Dataset
* **Name:** data_science_job.csv
* **Target Columns (< 5% missing & MCAR):**
  * `city_development_index` (Numerical)
  * `enrolled_university` (Categorical)
  * `education_level` (Categorical)
  * `experience` (Numerical)
  * `training_hours` (Numerical)

### Validation Methodology
To ensure that CCA did not alter the underlying data distribution, the data profile was evaluated before and after dropping the rows.

* **Numerical Columns:** Plotted using histograms with `density=True` to overlay probability density functions (PDF). The shape, variance, and mean of the distributions for `city_development_index` and `training_hours` remained identical post-CCA.
* **Categorical Columns:** Computed the ratio of each category within `education_level` and `enrolled_university`. The relative proportions of categories before and after dropping rows remained constant, confirming that no systematic bias was introduced.

---

## Conclusion
When data meets the MCAR assumption and falls below the 5% threshold, CCA is a simple and effective method. By verifying that the density distributions (for numerical data) and category ratios (for categorical data) remain unchanged, we validate that the subset of complete cases is representative of the original population.

---

## Repository Structure

```text
AI-ML_Journey/
└── Day_16_Complete_Case_Analysis/
    ├── README.md
    ├── day_16_complete_case_analysis.ipynb
    └── data_science_job.csv