# Day 18: Outlier Detection & Removal

## Quick Logic & Formulas

### 1. Z-Score
* **Use Case:** Normal Distribution (`cgpa`)
* **Formula:** $Z = \frac{X - \mu}{\sigma}$
* **Cutoff:** $|Z| > 3$
* **Strategy:** Trim or Cap at $\mu \pm 3\sigma$

### 2. IQR
* **Use Case:** Skewed Distribution (`placement_exam_marks`)
* **Formula:** $IQR = Q_3 - Q_1$
* **Cutoff:** * Lower Limit = $Q_1 - 1.5 \times IQR$
  * Upper Limit = $Q_3 + 1.5 \times IQR$
* **Strategy:** Trim or Cap at limits

### 3. Percentile
* **Use Case:** Distribution-Agnostic (`height`)
* **Cutoff:** * Lower Limit = 1st Percentile
  * Upper Limit = 99th Percentile
* **Strategy:** Trim or Cap (Winsorization) at boundaries

## Repository Structure

```text
├── data/
│   ├── placement.csv              # Used for Z-score and IQR analysis
│   └── weight-height.csv          # Used for Percentile-based analysis
├── notebooks/
│   ├── 01_outlier_z_score.ipynb   # Analysis on normally distributed 'cgpa'
│   ├── 02_outlier_iqr.ipynb       # Analysis on right-skewed 'placement_exam_marks'
│   └── 03_outlier_percentile.ipynb# Analysis on 'height' using 1st/99th thresholds
└── README.md