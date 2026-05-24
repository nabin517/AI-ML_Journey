# Day 04: Exploratory Data Visualization (Categorical Comparisons & Numerical Distributions) with Matplotlib and Seaborn

## Project Overview
This module establishes the foundational layer for exploratory data analysis (EDA) using Python's core visualization libraries: Matplotlib and Seaborn. The focus is centered on translating raw numerical arrays, Pandas DataFrames, and structural records into human-readable charts to evaluate data spreads, categorical volumes, and sequential trend lines before model ingestion.

Mastering canvas architecture, plot labels, and foundational distribution plots ensures accurate insights can be communicated clearly to team members and stakeholders.

---

## Core Concepts Implemented

### 1. Sequential Trend Mapping (Line Plots)
We implemented single and multi-series line plots to track metrics across intervals:
* **Dual Axis Configuration:** Testing plot behaviors across alternating dimensions, such as placing independent variables on both horizontal and vertical orientation constraints.
* **Multi-Series Overlaying:** Merging multiple data trends (e.g., mapping Temperature and Humidity over Days concurrently) onto a single coordinate canvas with unique colors, line styles, and distinct data markers.
* **DataFrame Integration:** Direct structural plotting pulling metrics explicitly from tabular Pandas DataFrame columns.

### 2. Volumetric Metrics (Categorical Bar Charts)
We implemented group comparisons to evaluate localized quantities across distinct categorical buckets:
* **Custom Color Arrays:** Mapping discrete color lists across multi-region arrays to group categories visually.
* **Axis Labels:** Formatting discrete textual axis markings to prevent truncation across non-numeric data arrays.

### 3. Density Tracking (Histograms & KDE)
We evaluated continuous variations across numerical data sets to observe grouping weights and tendencies:
* **Bin and Interval Structuring:** Adjusting bin widths and total counts dynamically to control the grouping resolutions of numeric scores.
* **Kernel Density Estimation Overlaying (KDE):** Computing a continuous probability density curve directly over rigid histogram blocks to visualize trend continuity.

### 4. Contextual Canvas Customization
We added metadata details to transform plain charts into readable informational maps:
* **Target Benchmarking (axvline):** Injecting exact structural threshold markers (e.g., drawing a vertical dashed line to divide passing and failing marks explicitly).
* **Legend Compilation:** Utilizing the plt.legend routine to extract label declarations from lines and blocks automatically into an organized visual key.
* **Canvas Grids:** Turning on coordinate grids (plt.grid) and setting global plot themes (sns.set_theme) to enable immediate structural scannability.

---

## Repository Structure
```text
AI-ML_Journey/
└── Day-04_Visualization-Basics/
    ├── README.md               # Engineering documentation
    └── exploratory_plots.ipynb # Trend lines, bars, and distribution notebook