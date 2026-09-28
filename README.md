# MP-EVData: Electric Vehicle Charging Load Analysis

## Project Overview

This project performs a reproducible analysis of electric vehicle (EV) charging load profiles using the MP-EVData dataset.

The objective is to characterize charging behaviors of different EV charging station types, identify daily charging patterns, classify station categories, interpret machine learning results, and evaluate charging load simultaneity.

The analysis includes:

- Data preprocessing and quality checks
- Station-level load profile analysis
- Time-level charging behavior analysis
- Daily charging pattern clustering
- Machine learning based station classification
- SHAP-based model interpretation
- Charging simultaneity analysis
- Time-of-use (TOU) price response analysis


## Dataset

Dataset: MP-EVData  
Source: Scientific Data (2026)  
Location: China  
Study year: 2024  
Time resolution: 15 minutes


### Station Types

The dataset contains multiple EV charging station archetypes:

- Taxi charging stations
- Bus charging stations
- Residential charging stations
- Battery swap stations
- Heavy-duty truck charging stations


## Project Structure

```
MP_EVData_Project/

├── README.md

├── notebooks/
│   └── 01_MP_EVData_Reproducible_Analysis.ipynb

├── data/
│   └── Raw dataset files (not included)

├── results/
│   ├── kmeans_results/
│   ├── rf_shap_results/
│   ├── simultaneity_results/
│   └── tou_price_response_results/

├── figures/
│   └── Generated analysis figures

├── report/
│   └── figures_used/

└── downloaded_zips/
    └── Original downloaded dataset archives
```


## Methodology

### 1. Data Quality Assessment

Performed checks include:

- Timestamp validation
- Missing interval detection
- Year coverage verification
- Station data consistency checks


### 2. Load Profile Analysis

Analyzed:

- Annual station load curves
- Average daily charging profiles
- Station type comparisons
- Peak demand characteristics


### 3. Charging Pattern Clustering

Applied:

**K-means clustering**

to identify representative daily charging behaviors.

Outputs:

- Daily charging shape clusters
- Cluster frequency analysis


### 4. Station Type Classification

Implemented:

**Random Forest classifier**

to classify charging stations based on extracted load features.

Evaluation includes:

- Classification performance
- Confusion matrices
- Feature importance analysis


### 5. Model Interpretation

Applied:

**SHAP (SHapley Additive exPlanations)**

to interpret machine learning decisions and identify important charging behavior features.


### 6. Charging Simultaneity Analysis

Calculated:

- Individual station peak loads
- Combined system peak load
- Simultaneity coefficient
- Station contribution to combined peak demand


## Key Results

The analysis generated:

- Station load pattern visualization
- Station type comparison figures
- K-means charging pattern clusters
- Random Forest classification results
- SHAP interpretation plots
- Simultaneity analysis results


## Reproducibility

All analysis steps are implemented in:

```
notebooks/01_MP_EVData_Reproducible_Analysis.ipynb
```

The notebook contains:

- Data loading
- Data cleaning
- Feature generation
- Statistical analysis
- Machine learning models
- Visualization generation


## Software Environment

Main tools:

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SHAP
- Jupyter Notebook


## Outputs

Generated figures are stored in:

```
figures/
```

Analysis tables and model outputs are stored in:

```
results/
```


## Author

Research project in:

**Management Science & Engineering**

Focus areas:

- Electric Vehicle Charging Systems
- Energy Data Analytics
- Machine Learning
- Sustainable Transportation
