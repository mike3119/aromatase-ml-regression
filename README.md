# Aromatase Inhibitor — Machine Learning Regression Analysis (MSR & R² Evaluation)

This repository contains a **supervised machine learning regression analysis** of Aromatase inhibitors using multiple models.  
The notebook used for this analysis is included as `aromataseB.ipynb`.

It compares various regression algorithms based on **MSR (Mean Squared Residuals ≈ MSE)** and **R² (Coefficient of Determination)** to identify which performs best for predicting aromatase-related activity.



## 📘 Project Summary

- **Objective:** Predict and analyze Aromatase inhibitor outcomes using regression-based ML models.  
- **Data Source:** Processed molecular data (loaded within the notebook).  
- **Evaluation Metrics:**  
  - **MSR / MSE** — measures average squared prediction error.  
  - **R² Score** — measures how well the model explains the variance of the data.  



## ⚙️ Models Evaluated

The notebook trained and evaluated the following models:
- Support Vector Regressor (**SVR**)
- ExtraTreeRegressor (multiple variants)
- ExtraTreesRegressor
- GradientBoostingRegressor
- DecisionTreeRegressor
- XGBRegressor
- KNeighborsRegressor
- MLPRegressor
- LinearSVR
- SGDRegressor



## 📊 Results Summary

The top-performing models (by **Test R²**) from the notebook are shown below:

| Model | Train MSE (≈ MSR) | Train R² | Test MSE (≈ MSR) | Test R² |
|:--|--:|--:|--:|--:|
| SVR | 0.782579 | 0.551344 | 1.061522 | 0.413114 |
| ExtraTreeRegressor3 | 0.782579 | 0.551344 | 1.061522 | 0.413114 |
| ExtraTreesRegressor2 | 0.782579 | 0.551344 | 1.061522 | 0.413114 |
| ExtraTreeRegressor1 | 0.782579 | 0.551344 | 1.061522 | 0.413114 |
| GradientBoostingRegressor | 0.841112 | 0.517786 | 1.221255 | 0.412216 |

**Best Model (Test R²):** SVR (0.413)  
**Lowest MSR (Test):** ExtraTreeRegressor variants (~1.06)



## 📈 Visualizations

Two plots summarize the performance of all regressors:

- **`figures/test_r2_by_model.png`** → Test R² comparison  
- **`figures/test_mse_by_model.png`** → Test MSE (≈ MSR) comparison

These visuals show how well each model generalizes to unseen data.



## 🧠 Insights

- Models with **higher Test R²** and **lower Test MSE (MSR)** perform best.  
- Tree-based models like **ExtraTreeRegressor** and **GradientBoostingRegressor** show solid performance but may overfit.  
- Simpler models (e.g., **LinearSVR**) perform less effectively on this dataset.  
- The gap between Train and Test results indicates the complexity of the data.



## 🧪 Reproduction

If you want to reproduce or modify this analysis:
1. Open the provided notebook:
   ```bash
   notebooks/aromataseB.ipynb

aromatase-ml-regression/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── aromataseB.ipynb
├── results/
│   ├── model_metrics.csv
│   └── model_metrics_table.md
├── figures/
│   ├── test_r2_by_model.png
│   └── test_mse_by_model.png
└── src/
    └── parse_notebook_metrics.py


🧩 Technologies Used

Python

Pandas

NumPy

Scikit-Learn

XGBoost

Matplotlib


🧬 Purpose of This Study

Aromatase is an enzyme critical in estrogen biosynthesis.
Understanding inhibitors through data-driven modeling can aid in developing better therapeutic candidates for hormone-dependent cancers.
This project explores how machine learning can be applied to analyze and predict inhibitory activities.

👨🏽‍🔬 Author

Akosu Michael Hemen
Machine Learning Researcher | Computational Chemist
