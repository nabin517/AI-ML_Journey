# Day 05: Advanced Data Visualization for Data Science

## Project Overview
This module covers advanced data visualization techniques using Matplotlib and Seaborn. Moving past basic lines and bars, this project focuses on Exploratory Data Analysis (EDA)—using complex charts to discover hidden patterns, relationships, and outliers in a dataset before feeding it into Machine Learning algorithms.

---

## Visualizations Covered & Purpose

### 1. Scatter Plots (`sns.scatterplot`)
* **Purpose:** Compares two continuous numeric features to check for linear or non-linear relationships. 
* **ML Value:** Used to test if features are mathematically ready for algorithms like Linear Regression.

### 2. Box Plots & Violin Plots (`sns.boxplot`, `sns.violinplot`)
* **Purpose:** Box plots display the median, quartiles, and explicit statistical outliers. Violin plots show the exact probability density and shape of the data spread.
* **ML Value:** Critical for detecting and removing extreme outlier values that could corrupt model training.

### 3. Heatmaps & Correlation Matrices (`sns.heatmap`)
* **Purpose:** A colored grid representing how strongly every single numeric column correlates with every other column.
* **ML Value:** Identifies redundant features (multi-collinearity) so we can drop duplicate data before training.

### 4. Pair Plots (`sns.pairplot`)
* **Purpose:** Automatically generates an all-in-one matrix grid of scatter plots and histograms for every single numeric feature combination instantly.
* **ML Value:** Provides a complete structural snapshot of the entire dataset at the very start of a project.

---

## Repository Structure
```text
AI-ML_Journey/
└── Day-05_Advanced-Visualization/
    ├── README.md               # Visualizations documentation
    └── advanced_plots.ipynb    # Jupyter Notebook with Seaborn/Matplotlib code