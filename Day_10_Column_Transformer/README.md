#  Day 10: Demystifying Data Preprocessing Pipelines

Welcome to Day 10 of my AI-ML Journey! Today, I tackled the complexities of categorical encoding and missing value imputation. To truly understand the mechanics under the hood, I first engineered the feature engineering pipeline **manually** before refactoring the codebase using Scikit-Learn's powerful `ColumnTransformer`.

##  Project Overview
Using the `covid_toy` dataset, the objective is to predict whether a patient has COVID-19 (`has_covid`) based on physical and geographical features. The dataset presents an excellent mix of numerical, nominal categorical, and ordinal categorical data, complete with missing values.

### Dataset Features:
* **`age`**: Numerical feature (Continuous)
* **`fever`**: Numerical feature (Contains missing values)
* **`gender`**: Nominal Categorical (2 unique values)
* **`city`**: Nominal Categorical (4 unique values)
* **`cough`**: Ordinal Categorical (Ordered: `mild` < `strong`)
* **`has_covid`**: Target Variable (Binary Label)

---

##  The Engineering Challenge: Manual vs. Automated

### The Hard Way (Manual Preprocessing & Concatenation)
Before leveraging high-level wrappers, I manually executed the transformations to master NumPy array shapes and dimension alignment:
1.  **Imputation**: Filled missing `fever` values using `SimpleImputer(strategy='mean')`.
2.  **One-Hot Encoding**: Encoded `gender` and `city` using `OneHotEncoder(drop='first', sparse_output=False)`. Dropping the first category strictly optimized the array structure to prevent multi-collinearity.
3.  **Ordinal Encoding**: Mapped `cough` categories (`mild` and `strong`) into a logical integer scale using `OrdinalEncoder`.
4.  **The Reshape & Concatenation Battle**: Faced and resolved the infamous `axis 1 is out of bounds for array of dimension 1` error. Because raw numerical and ordinal features extract as 1D arrays `(80,)`, I manually aligned their dimensions into 2D column vectors `(80, 1)` using `.reshape(-1, 1)` before executing an `np.concatenate(..., axis=1)`. The final manual matrix resulted in a precise shape of `(80, 7)`.

### The Smart Way (Using `ColumnTransformer`)
Refactored the manual spaghetti code into a clean, automated, production-ready pipeline using `ColumnTransformer`. This encapsulated the entire multi-type workflow into a single block, mitigating data leakage risks and eliminating manual dimension shaping entirely.

---

##  Repository Structure

```text
AI-ML_Journey/
└── Day-10_Column-Transformer/
    ├── README.md                      
    ├── column_transformer.ipynb # Notebook: Implementing          ColumnTransformer 
    └── covid_toy.csv          # Dataset containing both numerical and text columns                 