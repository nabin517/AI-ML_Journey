# AI-ML Journey: Day 14 - Advanced Feature Engineering (Mixed Variables)

## Overview
On Day 14, the focus was on handling Mixed Variables—columns that contain both numeric and categorical data within the same feature. Standard machine learning algorithms cannot process these hybrid formats directly. 

Using the Titanic Dataset, I engineered a custom feature `number` alongside existing mixed variables (`Cabin`, `Ticket`) and systematically decoupled them into distinct, model-ready numeric and categorical components.

---

## The Engineering Problem & Solution

### 1. Custom Feature: `number`
* **Logic:** If a passenger travelled alone, the value is 'A' (Categorical). If they travelled with family, the value is an integer representing the family size (Numerical).
* **Splitting Strategy:**
  * `number_categorical`: Retains 'A', assigns NaN to numeric values.
  * `number_numeric`: Retains the integer, assigns NaN to 'A'.

### 2. Standard Titanic Features (Cabin & Ticket)
* **Cabin**: Split into `cabin_num` (numerical) and `cabin_cat` (the deck letter).
* **Ticket**: Extracted the numeric ticket sequence and the string prefix into separate features.

---

## Repository Structure
```text
AI-ML_Journey/
└── Day-14_Mixed-Variables/
    ├── README.md                      
    ├── day_14_mixed_variables.ipynb    # Notebook: Splitting Mixed Variables & Feature Engineering
    └── titanic.csv                     # Dataset containing mixed variable inputs


