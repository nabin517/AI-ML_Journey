# Day 02: Foundational Numerical Computing & Multi-Dimensional Array Mechanics with NumPy

## Project Overview
This module establishes the core mathematical foundation for numerical computing using Python's NumPy library. The focus is centered on moving away from standard Python loops and toward vectorized, multi-dimensional array structures. 

Understanding raw memory layout, data casting, and multi-dimensional matrix slicing ensures highly optimized data structures before stepping into tensor operations and neural network weights.

---

## Core Concepts Implemented

### 1. Array Initialization & Structural Variants
We implemented various array generation strategies to establish dense data matrices directly in memory:
* **Standard Conversions:** Transforming Python lists into 1D arrays and nested lists into structured 2D matrices.
* **Pre-Allocation Routines:** Initializing standard matrices filled entirely with zeros (np.zeros) and ones (np.ones) to reserve explicit blocks of memory for incoming computational steps.
* **Sequential Generation:** Generating predictable numerical ranges using np.arange and creating perfectly linearly spaced numerical arrays using np.linspace.

### 2. Microscopic Array Attributes
Every NumPy array maintains strict structural attributes that define its memory consumption and alignment. We mapped and analyzed these core structural properties:
* **shape & size:** Extracting exact structural dimensions (rows, columns) and total element count.
* **ndim:** Tracking the physical geometric axes/dimensions of the initialized matrix.
* **dtype:** Ensuring data continuity by identifying the underlying byte allocation types (e.g., int64, float64).
* **itemsize & nbytes:** Measuring the exact byte-footprint of an individual item and the total cumulative memory footprint of the entire matrix block.

### 3. Spatial Slicing & Matrix Indexing
We mapped out precise indexing coordinates across multi-dimensional coordinate spaces:
* **1D Sequences:** Implementing standard interval slicing techniques to isolate subsets of data.
* **2D Matrix Subsets:** Accessing specialized coordinates within rows and columns simultaneously. We focused on utilizing row and column boundaries (e.g., matrix[row_start:row_end, col_start:col_end]) to crop rectangular subsets of a 2D matrix without breaking data continuity.

---

## Repository Structure
```text
AI-ML_Journey/
└── Day-02_Numpy_Basics/
    ├── README.md               # Engineering documentation
    └── numpy_fundamentals.ipynb # Vectorized array initialization and slicing notebook