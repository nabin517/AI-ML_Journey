Simple Linear Regression: CGPA vs Placement Package
📌 Project Overview
This project implements Simple Linear Regression using Python and Scikit-learn to explore the relationship between a student's CGPA and their placement package.
The objective is to understand how a single numerical feature (CGPA) can be used to predict a continuous target variable (placement package).
This project is part of my AI/ML learning journey as I work toward becoming job-ready in Machine Learning and Data Science.
🎯 Objectives
	•	Understand and implement Simple Linear Regression.
	•	Explore the relationship between CGPA and placement package.
	•	Split data into training and testing sets.
	•	Train a regression model using Scikit-learn.
	•	Make predictions on unseen test data.
	•	Evaluate performance using regression metrics.
	•	Visualize the fitted regression line.
🛠️ Technologies Used
	•	Python
	•	NumPy
	•	Pandas
	•	Matplotlib
	•	Scikit-learn
	•	Jupyter Notebook
📂 Project Structure
simple-linear-regression-cgpa-placement/
│
├── placement1.csv
├── simple_linear_regression.ipynb
├── README.md
└── requirements.txt
Note: Include placement1.csv only if you have permission to redistribute the dataset. Otherwise, provide instructions and a link to the original dataset.
📊 Dataset
The dataset contains information used to examine the relationship between:
	•	CGPA: The input feature.
	•	Package: The target variable representing placement package.
The dataset is loaded using Pandas, and incomplete rows in the selected columns are removed before training.
Dataset source: [Add the original Kaggle dataset link here.]
⚙️ Project Workflow
1. Data Loading and Exploration
Loaded the dataset using Pandas and inspected the initial rows to understand its structure.
2. Data Visualization
Created a scatter plot to visualize the relationship between CGPA and placement package.
3. Feature and Target Selection
	•	Feature (X): CGPA
	•	Target (y): Placement package
4. Train-Test Split
Split the data into training and testing sets using an 80:20 ratio, with random_state=42 for reproducibility.
5. Model Training
Trained a LinearRegression model using the training data.
The model learns the relationship:
[ \hat{y} = b_0 + b_1x ]
Where:
	•	(\hat{y}) is the predicted placement package.
	•	(b_0) is the intercept.
	•	(b_1) is the learned coefficient (slope).
	•	(x) is the student's CGPA.
6. Prediction and Evaluation
Generated predictions on the held-out test set and evaluated the model using:
Metric
Purpose
MAE
Measures average absolute prediction error.
MSE
Measures average squared prediction error.
RMSE
Expresses error in the target's original units.
R²
Compares the model with a baseline that predicts the test-set mean.
7. Visualization of the Fitted Model
Plotted the observed data and the fitted regression line to visualize the relationship captured by the model.
📈 Results
After running the notebook, record the actual results below.
	•	Slope: [Insert actual coefficient]
	•	Intercept: [Insert actual intercept]
	•	Test MAE: [Insert actual value]
	•	Test MSE: [Insert actual value]
	•	Test RMSE: [Insert actual value]
	•	Test R²: [Insert actual value]
These metrics describe the model's performance on the selected test set. Their practical interpretation depends on the dataset, package units, and the quality of the data.
🧠 Key Learnings
Through this project, I practiced:
	•	Implementing Simple Linear Regression with Scikit-learn.
	•	Understanding coefficients and intercepts.
	•	Separating features and target variables.
	•	Using train-test splitting to evaluate generalization.
	•	Calculating regression evaluation metrics.
	•	Visualizing a fitted regression line.
	•	Recognizing the limitations of predictions based on a single feature.
⚠️ Limitations
	•	The model uses only CGPA to predict placement package.
	•	Placement outcomes may also depend on skills, experience, interview performance, company, and other factors.
	•	A linear relationship may not fully represent the underlying data.
	•	Evaluation results depend on the dataset and train-test split.
	•	The model demonstrates an association, not a causal relationship.
🚀 Future Improvements
	•	Explore additional relevant features.
	•	Check for missing values, outliers, and unusual observations.
	•	Compare Simple Linear Regression with Multiple Linear Regression.
	•	Use cross-validation for a more robust assessment.
	•	Compare against a baseline model.
	•	Experiment with other suitable regression algorithms.
👨‍💻 Author
Computer Engineering Student | Aspiring AI/ML Engineer
This project is part of my ongoing journey to build practical Machine Learning skills through hands-on projects.
If you find this project useful, feel free to explore the notebook and share feedback!
