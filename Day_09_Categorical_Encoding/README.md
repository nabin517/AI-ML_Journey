# Day 09: Categorical Encoding (Ordinal, One-Hot, and Label Encoding)

## Project Overview
This module dives into **Categorical Encoding**, a critical feature engineering step. Because Machine Learning algorithms are purely mathematical models, they cannot read text strings like "Toyota", "High School", or "Yes". This project implements and compares **Ordinal Encoding**, **Label Encoding** (on customer feedback data), and **One-Hot Encoding** (on car resale data) to transform text categories into numbers without losing essential information.

## Encodings Covered & Purpose

### 1. Ordinal Encoding & Label Encoding
* **Dataset Used:** `customer_data.csv` (Features: `age`, `gender`, `review`, `education`, `purchased`)
* **What it does:** * **Ordinal Encoding:** Used for text columns that have a natural, mathematical order or ranking (e.g., `education` mapped as *High School = 0, UG = 1, PG = 2* or `review` mapped as *Poor = 0, Average = 1, Good = 2*).
  * **Label Encoding:** Specifically used to transform the target label column (e.g., converting the `purchased` column's *No/Yes* into *0/1*).
* **ML Value:** Preserves the step-by-step mathematical relationship of ranked data, allowing the model to understand that "PG" represents more education than "High School".

### 2. One-Hot Encoding (Nominal Encoding)
* **Dataset Used:** `cars_data.csv` (Features: `brand`, `km_driven`, `fuel`, `owner`, `selling_price`)
* **What it does:** Used for text columns with no inherent order or ranking (e.g., `brand` like *Maruti, Hyundai, Toyota* or `fuel` like *Petrol, Diesel*). It splits each unique category into its own brand-new column of `0`s and `1`s (dummy variables) without using a Column Transformer.
* **ML Value:** Prevents the model from making false mathematical assumptions. If we assigned numbers like 1, 2, and 3 to Maruti, Hyundai, and Toyota, the model would mistakenly think Toyota (3) is "greater than" Maruti (1). One-Hot Encoding keeps them perfectly equal.

---

##  Why Correct Encoding Matters for ML Accuracy

1. **Eliminating Bias:** Using One-Hot encoding on nominal data prevents distance-based models from introducing artificial rankings between unrelated categories (like car brands or fuel types).
2. **Preserving Order:** Using Ordinal encoding ensures tree-based models or linear models can exploit the natural progression inherent in ranked tracking data (like education level or review quality).
3. **Target Compatibility:** Label Encoding formats binary output choices perfectly for classification loss functions, ensuring clean performance evaluation metrics.

## Repository Structure

AI-ML_Journey/
└── Day-09_Categorical-Encoding/
    ├── README.md                       
    ├── ordinal_label_encoding.ipynb    # Notebook: Ordinal & Label Encoder on Customer Data
    ├── customer_data.csv               # Dataset containing customer reviews and education
    ├── one_hot_encoding.ipynb          # Notebook: One-Hot Encoding on Car Data
    └── cars_data.csv                   # Dataset containing vehicle specifications