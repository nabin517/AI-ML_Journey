# Pandas Basics: Data Cleaning and Exploration

## What is this project?
This project is a complete guide to cleaning and managing data using the **Pandas** library in Python. Before building any Machine Learning or Deep Learning models, the data must be clean and organized. This project shows how to take a raw dataset and fix common issues like missing information, duplicate entries, and incorrect formats.

## What operations did I perform?

### 1. Loading the Data & Creating Structures
- Created basic data structures from scratch using Pandas **Series** (1D arrays) and **DataFrames** (2D tables).
- Loaded a raw dataset (`.csv` file) into Python.

### 2. Understanding the Data
- Used `.head()` to look at the first few rows of data.
- Used `.info()` to check the data types and see how the columns are structured.
- Used `.describe()` to get quick statistical summaries (like mean, min, and max values).

### 3. Cleaning Messy Data
- **Checked for Missing Values:** Counted how many blank spaces or missing values exist in each column.
- **Removed Bad Rows:** Dropped rows that contained missing data where it couldn't be fixed.
- **Filled Categorical Missing Data:** Replaced missing values in text columns with the **Mode** (the most frequent value in that column).
- **Removed Duplicates:** Found and deleted identical repeated rows to keep the data unique.

### 4. Sorting and Transforming Data
- **Renamed Columns:** Changed column headers to make them cleaner and easier to read.
- **Filtered Rows:** Extracted specific rows based on conditions (for example, selecting only rows that match a certain criteria).
- **Sorted Values:** Arranged the data in order based on specific columns.
- **Applied Custom Functions:** Used the `.apply()` function to change data values dynamically across rows.

## What's inside this folder?
- `Learning_pandas.ipynb`: The Jupyter Notebook containing all the Python code and step-by-step notes.
- `sample_dataset.csv`: The raw data file used to test and run the code.

