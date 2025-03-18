# IIT-KGP-Hackathon

# Materials Informatics Analysis

---

## Problem
The goal of this project is to analyze electronic band gap properties of materials using machine learning. Specifically, we address two key challenges:
1. **Binary Classification**: Identify whether a material is an insulator (band gap ≥ 0.5 eV).
2. **Regression**: Predict the continuous band gap values for insulating materials.

The dataset contains **1031 materials** with **37 atomic-level features**, including electronegativity, HOMO/LUMO energies, atomic Z radii, and magnetic moment (μ).

---

## Solution
### Binary Classification
- **Model**: XGBoost Classifier.
- **Preprocessing**: SMOTE for handling class imbalance and StandardScaler for feature scaling.
- **Results**:
  - Accuracy: 91.46%.
  - Key Features: Atomic electron affinity, Atomic Z radii, Basis HOMO energy, Magnetic moment.

### Regression
- **Model**: XGBoost Regressor.
- **Preprocessing**: StandardScaler for feature scaling.
- **Results**:
  - R² Score: 0.883.
  - MSE: 0.016.
  - Key Features: Magnetic moment, Atomic Z radii, Basis HOMO energy, Atomic HOMO energy.

### Feature Importance
- SHAP (SHapley Additive exPlanations) was used to interpret the models and identify the most important features driving predictions.

---
