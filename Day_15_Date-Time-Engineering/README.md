# Day 15: Mastering Date and Time Engineering in Python

## Project Overview
Raw datasets frequently contain temporal information trapped in `string` or `object` formats. This format restricts any meaningful analytical or predictive capabilities. On Day 15 of my AI/ML journey, I built a dedicated data preprocessing module designed to parse, transform, and extract high-value features from complex date and time components.

This module converts static strings into dynamic, multi-dimensional inputs ready for Machine Learning pipelines.

---

## Key Features & Implementations

### 1. Temporal Type Conversion
* Identified and parsed `string`/`object` datatypes from messy data fields (`Order Date` and `Message Time`).
* Standardized text formats into robust, high-performance `datetime64[ns]` objects using Pandas.

### 2. Advanced Date Feature Engineering
Extracted granular, categorical, and cyclical features from the structured date objects:
* **Chronological Milestones:** Year, Month, Day.
* **Contextual Metrics:** Day of the week, Month name.
* **Duration Benchmarks:** Calculated the exact number of weeks elapsed from a historical date to the present day.

### 3. High-Precision Time Delta Extraction
* Deconstructed time components into isolated metrics: Hour, Minute, and Second.
* Engineered real-time features tracking **Time Elapsed** between two distinct events.
* Calculated absolute time deltas relative to the current timestamp, down to the exact second.

---

## Repository Structure
```text
AI-ML_Journey/
└── Day_15_Date-Time-Engineering/
    ├── README.md                      
    ├── day_15_datetime_engineering.ipynb  # Notebook: Parsing, Deconstructing, and Time Delta Extraction
    ├── messages.csv                       # Dataset containing raw message time inputs
    └── orders.csv                         # Dataset containing raw order date inputs