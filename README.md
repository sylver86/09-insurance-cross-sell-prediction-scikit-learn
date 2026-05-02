# Insurance Cross-Sell Prediction — ML Model Comparison

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-F37626?logo=jupyter&logoColor=white)

## Overview

Predictive model for a **vehicle insurance cross-sell campaign**: given a customer's health insurance history and demographic profile, predict whether they would be interested in purchasing vehicle insurance.

The project covers the full ML lifecycle — clustering for target variable construction, systematic comparison of 8 classification algorithms, and a clear selection rationale based on measurable performance metrics.

---

## Model Comparison

| Model | Accuracy | F1 Score | Notes |
|-------|----------|----------|-------|
| Naive Bayes (Bernoulli) | ~0.76 | ~0.72 | Baseline |
| Naive Bayes (Gaussian) | ~0.78 | ~0.74 | |
| SVC — Linear kernel | ~0.83 | ~0.81 | |
| SVC — Polynomial kernel | ~0.82 | ~0.80 | |
| SVC — Sigmoid kernel | ~0.79 | ~0.76 | |
| **SVC — RBF kernel** | **~0.87** | **~0.85** | **Best overall** |
| Neural Network (MLP) | ~0.86 | ~0.84 | Close second |
| K-Nearest Neighbours | ~0.81 | ~0.78 | |

> **SVC with RBF kernel** achieved the best balance of accuracy and generalisation on the held-out test set.

---

## Project Workflow

```
Raw customer dataset (380K+ records)
        │
        ▼
  1. Data Preprocessing
     • Missing value handling, feature normalisation
     • Categorical encoding (gender, vehicle age, damage)
        │
        ▼
  2. Customer Clustering (K-Means + Hierarchical)
     • Segment customers by behavioural profile
     • Define target variable from cluster analysis
        │
        ▼
  3. Model Training & Comparison
     • 8 algorithms trained and evaluated
     • Metrics: accuracy, precision, recall, F1
        │
        ▼
  4. Best Model Selection
     → SVC RBF Kernel (F1 ~0.85)
```

---

## Dataset

**Source:** Kaggle — Health Insurance Cross Sell Prediction
**Size:** ~380,000 customer records
**Features:** age, gender, driving licence, region, vehicle age, vehicle damage, annual premium, sales channel, customer vintage

Key challenge: **class imbalance** (~88% negative class) — addressed through class weighting and stratified sampling.

---

## Setup

```bash
git clone https://github.com/sylver86/09-insurance-cross-sell-prediction-scikit-learn.git
cd 09-insurance-cross-sell-prediction-scikit-learn
pip install scikit-learn pandas numpy matplotlib seaborn jupyter
jupyter notebook
```

Open `Progetto Machine Learning.ipynb` and run all cells.

---

## Technologies

`Python` · `Scikit-learn` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Jupyter`
