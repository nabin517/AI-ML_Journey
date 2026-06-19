# AI-ML Journey - Day 13: Power Transformers

This repository documents Day 13 of my AI-ML journey, focusing on feature engineering techniques to handle non-normal distributions in numerical data. Specifically, this project explores the impact of the **Box-Cox** and **Yeo-Johnson** power transformations on predictive performance using a Concrete Strength dataset.

## Mathematical Formulation

The Box-Cox transformation is a parametric power transformation technique used to stabilize variance and normalize data. For a given feature $x$, it is mathematically defined as:

$$y^{(\lambda)} = \begin{cases} \frac{x^\lambda - 1}{\lambda} & \text{if } \lambda \neq 0 \\ \ln(x) & \text{if } \lambda = 0 \end{cases}$$

> **Note:** The Box-Cox transformation strictly requires the input data to be positive ($x > 0$). For datasets containing zero or negative values, the Yeo-Johnson transformation is used instead.

## Project Overview

Many machine learning algorithms, including Linear Regression, assume that the input features are normally distributed. When data is skewed, model performance can degrade significantly. 

In this session, I implemented the Box-Cox transformation on a concrete dataset to stabilize variance and normalize errors.

### Key Deliverables & Insights
* **Baseline Performance:** A Linear Regression model trained on the raw, skewed features yielded an $R^2$ score of **0.46**.
* **Transformed Performance:** After applying the Box-Cox transformation to the features, the Linear Regression model's $R^2$ score improved to **0.66**.
* **Visual Validation:** Utilized Histogram and Q-Q (Quantile-Quantile) plots to verify normality. Features that originally exhibited strong skewness successfully shifted to a normal distribution post-transformation.

## Repository Structure

```text
AI-ML_Journey/
└── Day-13_Power_Transformers/
    ├── README.md
    ├── concrete_data.csv
    └── day13_power_transformer.ipynb