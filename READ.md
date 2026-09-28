# MP-EVData: Electric Vehicle Charging Load Analysis

## Project Overview

This project analyzes electric vehicle (EV) charging load profiles using the MP-EVData dataset.

The objective is to characterize charging behaviors of different EV charging station types, identify daily charging patterns, classify station categories using machine learning, interpret model decisions, and evaluate charging simultaneity.

---

# Dataset

## Dataset Information

**Dataset:** MP-EVData

**Source:** Scientific Data (2026)

**Dataset DOI:**  
10.6084/m9.figshare.29882366

## Dataset Coverage

- Year: 2024
- Location: China
- Time resolution: 15 minutes
- Number of analyzed stations: 8

## Station Types

The analyzed stations represent different charging behaviors:

- Taxi charging stations
- Bus charging stations
- Residential charging stations
- Battery swap stations
- Heavy-duty truck charging stations

---

# Project Structure


MP_EVData_Project/
├── README.md
├── notebooks/
│   └── 01_MP_EVData_Reproducible_Analysis.ipynb
├── data/
├── results/
│
│   ├── A1_results/
│   ├── taxi_comparison/
│   ├── bus_comparison/
│   ├── residential_results/
│   ├── battery_swap_results/
│   ├── truck_results/
│   ├── kmeans_results/
│   ├── rf_shap_results/
│   ├── simultaneity_results/
│   └── tou_price_response_results/
├── figures/
├── report/
│   └── figures_used/
└── downloaded_zips/

---

# Analysis Workflow

## 1. Data Preparation and Validation

The dataset was processed and checked before analysis.

Performed steps:

- Dataset extraction
- Timestamp verification
- Calendar year filtering
- Missing value checking
- 15-minute interval validation
- Station-level load preparation

---

# 2. EV Charging Load Profile Analysis

Station-level charging patterns were analyzed using power consumption data.

Analyses performed:

- Individual station load curves
- Annual charging behavior
- Average daily charging profiles
- Comparison between station types

Generated figures:

- `01_station_load_patterns.png`
- `02_station_type_comparison.png`

---

# 3. K-means Clustering Analysis

Daily charging curves were normalized and clustered using K-means.

Purpose:

To identify typical EV charging behavior patterns.

Generated outputs:

- Cluster centers
- Daily cluster assignments
- Cluster shape visualization
- Cluster summary statistics

Generated figure:

- `kmeans_results_cluster_shapes.png`

---

# 4. Random Forest Station Classification

A Random Forest machine learning model was developed to classify EV charging station categories.

Features used:

- Charging load characteristics
- Time-based charging behavior features

Model evaluation:

- Classification performance
- Confusion matrices
- Feature importance analysis

Generated outputs:

- Classification results
- Feature importance results

---

# 5. SHAP Model Interpretation

SHAP (SHapley Additive exPlanations) was applied to interpret the Random Forest model.

Purpose:

To understand which charging periods contribute most to station type classification.

Generated outputs:

- SHAP feature importance
- Important charging time slots

Generated figures:

- `rf_shap_results_shap_overall_importance.png`
- `rf_shap_results_confusion_matrices.png`

---

# 6. Charging Simultaneity Analysis

Charging simultaneity was evaluated to understand combined grid demand characteristics.

Calculated parameters:

- Individual station peak demand
- Combined system peak demand
- Simultaneity coefficient
- Station contribution at system peak

Generated outputs:

- Combined peak contribution table
- Simultaneity summary results

Generated figure:

- `simultaneity_contribution.png`

---

# 7. Time-of-Use (TOU) Price Response Analysis

The optional TOU analysis investigated charging behavior under different electricity tariff periods.

Analyses performed:

- Tariff period identification
- Charging concentration analysis
- Potential demand response behavior

Generated outputs:

- TOU tariff coverage audit
- Charging concentration results
- Price response analysis results

Generated figure:

- `tou_energy_concentration.png`

---

# Reproduction Instructions

## Required Python Libraries

Install required packages:

```bash
pip install pandas numpy matplotlib scikit-learn shap openpyxl
```

## Running the Analysis
Open:
notebooks/01_MP_EVData_Reproducible_Analysis.ipynb

Run notebook cells sequentially to reproduce:
1. Data validation
2. Load profile analysis
3. Station type comparison
4. K-means clustering
5. Random Forest classification
6. SHAP interpretation
7. Simultaneity analysis
8. TOU price response analysis
---

Repository Usage
Clone this repository:
git clone YOUR_GITHUB_REPOSITORY_LINK

Navigate to the project folder:
cd MP_EVData_Project

Open the analysis notebook:
notebooks/01_MP_EVData_Reproducible_Analysis.ipynb

Run the notebook to reproduce all results and figures.
---

Data Availability
The MP-EVData dataset should be downloaded separately from the original source.
Dataset DOI:
10.6084/m9.figshare.29882366
---

# License

This repository is intended for academic research and reproducibility purposes.

Please refer to the original MP-EVData dataset license for data usage conditions.
