# Day 23 – Hyperparameter Tuning using GridSearchCV
## Introduction
GridSearchCV is a Scikit-learn technique used to find the best hyperparameters for a machine learning model. It tests different parameter combinations using cross-validation and selects the combination with the best average score.
# What I Learned
	•	Why hyperparameter tuning is important.
	•	Parameters vs. hyperparameters.
	•	Cross-validation and 5-fold CV.
	•	GridSearchCV and its important parameters.
	•	Creating a parameter grid using param_grid.
	•	Using Pipeline with StandardScaler and Logistic Regression.
	•	Preventing data leakage during cross-validation.
	•	Understanding best_params_, best_score_, and best_estimator_.
	•	Evaluating the selected model on unseen test data.
# Practical Implementation
	•	Dataset: Breast Cancer Wisconsin dataset
	•	Model: Logistic Regression
	•	Preprocessing: StandardScaler
	•	Hyperparameter: C
	•	Candidate values: [0.01, 0.1, 1, 10, 100]
	•	Cross-validation: 5-fold
	•	Scoring metric: Accuracy
# Key Learning
Using Pipeline with GridSearchCV ensures that preprocessing is fitted separately within each cross-validation training fold, helping prevent data leakage.
# Tools and Libraries
	•	Python
	•	NumPy
	•	Pandas
	•	Scikit-learn
# Day 23 completed — Learning practical hyperparameter tuning with GridSearchCV.
