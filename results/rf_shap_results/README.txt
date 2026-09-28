Exploratory four-type Random Forest classification.
Inputs: 96 daily-total-normalized electrical load values.
Stations: A1/A2 taxi; A3/A4 bus; A5/A6 residential; A9/A10 truck.
Battery-swap count stations A7/A8 excluded from this baseline.
Fold 1 train: A1,A3,A5,A9; test: A2,A4,A6,A10.
Fold 2 reverses those training and test stations.
RF: 300 trees, min_samples_leaf=2, class_weight=balanced,
random_state=42; remaining parameters use library defaults.
SHAP: 20 test days per station per fold, random_state=42.
TreeExplainer: tree_path_dependent, model_output=raw.
SHAP reconstruction checked against predicted probabilities.
Overall importance averages absolute SHAP across days and classes.
Illustrative case: fold 1, A10, 2024-10-01; actual truck, predicted residential.
scikit-learn version: 1.6.1
SHAP version: 0.52.0
Only two stations per type; results are exploratory.
SHAP explains fitted predictions, not causal charging behaviour.
