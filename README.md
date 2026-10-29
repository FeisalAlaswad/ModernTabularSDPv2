# Do Modern Tabular Deep Learning Models Advance Software Defect Prediction?
### A Large-Scale Evaluation Across 17 Datasets

This repository contains the implementation used in our empirical study evaluating modern tabular deep learning models for **Software Defect Prediction (SDP)**. The framework benchmarks classical machine learning algorithms, deep tabular neural networks, transformer-based architectures, and ensemble methods across **17 publicly available NASA PROMISE and AEEEM datasets**.

---

## Overview

The pipeline performs the complete experimental workflow:

- Download and preprocess the NASA PROMISE and AEEEM datasets
- Harmonize datasets into a unified ARFF format
- Generate dataset statistics and visualizations
- Perform feature selection using Random Forest importance and SHAP
- Train and evaluate multiple machine learning models using stratified 5-fold cross-validation
- Compare results under different experimental settings
- Generate ensemble models
- Perform statistical significance testing
- Save all predictions, figures, and evaluation metrics automatically

---

## Repository Structure

```
.
├── Comprehensive_Software_Defects.ipynb
├── comprehensive_software_defects.py
├── README.md
├── LICENSE
└── outputs/
```

During execution, the pipeline automatically creates folders containing

```
defect_data/
feature_selection/
results_no_smote/
results_smote/
results_no_smote_feature_selection/
results_smote_feature_selection/
```

---

## Datasets

The pipeline automatically downloads:

- NASA PROMISE Software Defect Prediction datasets
- AEEEM Software Defect Prediction datasets

A total of **17 projects** are evaluated.

### NASA

- CM1
- JM1
- KC1
- KC3
- MC1
- MC2
- MW1
- PC1
- PC2
- PC3
- PC4
- PC5

### AEEEM

- EQ
- JDT
- LC
- ML
- PDE

---

## Evaluated Models

### Classical Machine Learning

- Logistic Regression
- Gaussian Naive Bayes
- Random Forest
- Extra Trees
- XGBoost
- LightGBM
- CatBoost

---

### Deep Tabular Learning

- TabNet
- GANDALF
- DANet

---

### Transformer-Based Models

- FT-Transformer
- TabTransformer
- AutoInt

---

### Ensemble Models

- Soft Voting
- Hard Voting
- Stacking
- Meta-Stacking

---

## Feature Selection

Feature selection combines

- Random Forest Feature Importance
- SHAP Values

For every dataset the pipeline produces

- Random Forest importance plot
- SHAP beeswarm plot
- SHAP importance plot
- Combined heatmap
- Importance CSV
- Automatically generated selected feature list

---

## Experimental Modes

The pipeline supports four execution modes.

| Mode | SMOTE | Feature Selection |
|------|-------|-------------------|
| 1 | ✗ | ✗ |
| 2 | ✓ | ✗ |
| 3 | ✗ | ✓ |
| 4 | ✓ | ✓ |

Simply modify

```python
EXECUTION_MODE = 1
```

inside the configuration section.

---

## Evaluation Protocol

All experiments use

- Stratified 5-fold Cross Validation
- Fixed random seed (42)
- Identical preprocessing across models

Evaluation metrics include

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Matthews Correlation Coefficient (MCC)
- Training time
- Inference time
- GPU memory usage

---

## Statistical Analysis

The pipeline performs

- Linear Mixed Effects Models

These analyses are used to determine statistically significant performance differences across model families.

---

## Requirements

Python 3.10+

Main dependencies

```
numpy
pandas
scikit-learn
imbalanced-learn
xgboost
lightgbm
catboost
torch
pytorch-tabnet
pytorch-tabular
shap
statsmodels
scikit-posthocs
matplotlib
seaborn
scipy
```

Install using

```bash
pip install -r requirements.txt
```

or

```bash
pip install pytorch_tabular pytorch_tabnet xgboost lightgbm catboost shap statsmodels scikit-posthocs imbalanced-learn
```

---

## Running the Pipeline

Execute

```bash
python comprehensive_software_defects.py
```

or open the notebook

```
Comprehensive_Software_Defects.ipynb
```

The script automatically

1. Downloads datasets
2. Converts AEEEM to ARFF
3. Merges datasets
4. Performs feature selection
5. Runs model benchmarking
6. Creates figures
7. Saves predictions
8. Produces statistical analyses

---

## Output

For every dataset, the framework automatically saves

- Predictions
- Confusion matrices
- ROC curves
- Precision–Recall curves
- Model summaries
- Fold-wise metrics
- Feature importance plots
- SHAP visualizations
- Performance tables
- Compressed ZIP archive of results

---

## Reproducibility

All experiments use

- Random seed = 42
- Stratified 5-fold cross-validation
- Consistent preprocessing
- Automatic dataset downloading
- Fully reproducible evaluation pipeline

---

## Citation

If you use this repository in your research, please cite:

```bibtex
@article{YOUR_CITATION,
  title={Do Modern Tabular Deep Learning Models Advance Software Defect Prediction? A Large-Scale Evaluation Across 17 Datasets},
  author={...},
  journal={...},
  year={2026}
}
```

---

## License

This project is released under the MIT License.

---

## Contact

**Feisal Alaswad**

Department of Computing Technologies

SRM Institute of Science and Technology

Email: *Add your email here*

---

If you find this repository useful, please consider giving it a ⭐.
