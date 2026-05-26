# Day 06: Titanic Dataset - Structural Audit & Univariate Analysis

## Project Overview
This module breaks the initial data exploration phase into two dedicated workflows across separate Jupyter Notebooks. The objective is to cleanly separate foundational data inspection (understanding the shape, health, and properties of the data) from structural visual profiling (analyzing individual feature distributions).

---

## Repository Pipeline & Notebook Breakdown

### Notebook 1: Data Inspection & Structural Audit (`01_data_understanding.ipynb`)
This notebook focuses on programmatic data profiling to audit the data's health and structural limits before any plotting begins.
* **Data Dimensions:** Checked dataset scale using `df.shape`.
* **Visual Sample:** Inspected the raw layout using `df.head()` and `df.tail()`.
* **Data Integrity:** Counted missing values with `df.isnull().sum()` and identified duplicate rows using `df.duplicated().sum()`.
* **Data Typer:** Verified column constraints using `df.dtypes`.
* **Descriptive Statistics:** Extracted central tendencies, spread, and percentiles via `df.describe()`.
* **Linear Associations:** Calculated initial multi-variable relations using `df.corr()`.

### Notebook 2: Univariate Visual Analysis (`02_univariate_analysis.ipynb`)
This notebook isolates variables one by one to visually map out their distribution shapes, scales, and frequency balances using Matplotlib and Seaborn.
* **Histograms & Distplots:** Profiled continuous metrics like Passenger Age and Fares, revealing a heavy right-skew in ticket prices.
* **Box Plots:** Leveraged to instantly isolate extreme statistical outliers in numeric columns.
* **Pie Charts:** Visualized structural proportions of categorical splits, including overall survival metrics and gender balance.

---

## Repository Structure
```text
AI-ML_Journey/
└── Day-06_Titanic-EDA/
    ├── README.md                  # Workflow and analysis documentation
    ├── 01_data_understanding.ipynb # Notebook 1: Structure and health audit
    └── 02_data_univariate.ipynb   # Notebook 2: Univariate visualization plots