# InsurePredict — Modello Predittivo per Cross-Selling Assicurativo

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikitlearn&logoColor=white)
![F1](https://img.shields.io/badge/F1--Score-~0.85-brightgreen)
![Models](https://img.shields.io/badge/Algorithms%20Compared-8-blue)

## Panoramica

Modello predittivo per identificare clienti assicurativi propensi all'acquisto di polizze auto (cross-selling), con confronto sistematico di 8 algoritmi di Machine Learning. Il vincitore — SVC con kernel RBF — raggiunge F1-Score ~0.85 su un dataset fortemente sbilanciato (gestito via SMOTE e class weighting).

Pipeline ML completa applicabile in contesti di Financial Services, Insurance e CRM enterprise: dalla feature engineering alla selezione del modello con metodologia rigorosa e riproducibile.

## Valore Enterprise

| Settore / Azienda | Rilevanza |
|-------------------|-----------|
| Insurance & Banking | Cross-sell/up-sell prediction su base clienti esistente |
| IT Consulting (Accenture, NTT Data) | Pipeline ML enterprise per Financial Services |
| Data Reply | ML model selection con gestione class imbalance |
| CRM & Marketing Analytics | Scoring propensity per campagne outbound |

## Risultati — Confronto 8 Algoritmi

| Algoritmo | F1-Score | Note |
|-----------|----------|------|
| **SVC RBF Kernel** | **~0.85** | **Miglior performance** |
| Random Forest | ~0.82 | |
| Gradient Boosting | ~0.81 | |
| Logistic Regression | ~0.76 | |
| K-Nearest Neighbors | ~0.74 | |
| Decision Tree | ~0.72 | |
| Naive Bayes | ~0.68 | |
| Linear SVC | ~0.67 | |

## Pipeline ML

```
Dataset grezzo (sbilanciato)
        │
        ▼
EDA + Feature Engineering
analisi correlazioni · encoding categoriche · scaling
        │
        ▼
Gestione Class Imbalance (SMOTE + class_weight)
        │
        ▼
Training 8 algoritmi (cross-validation)
        │
        ▼
Model Selection → SVC RBF (F1~0.85)
        │
        ▼
Valutazione finale: F1 · Precision · Recall · ROC-AUC · Confusion Matrix
```

## Setup

```bash
git clone https://github.com/sylver86/09-insurance-cross-sell-prediction-scikit-learn.git
cd 09-insurance-cross-sell-prediction-scikit-learn
pip install -r requirements.txt
jupyter notebook "notebooks/Progetto Machine Learning.ipynb"
```

## Struttura Repository

```
09-insurance-cross-sell-prediction-scikit-learn/
├── notebooks/
│   └── Progetto Machine Learning.ipynb
├── data/
│   └── insurance_cross_sell.csv
├── requirements.txt
└── README.md
```

## Stack Tecnologico

`Python 3.8+` · `scikit-learn` · `imbalanced-learn (SMOTE)` · `pandas` · `NumPy` · `Matplotlib` · `Seaborn`

---

---

# InsurePredict — Insurance Cross-Sell Prediction Model 🇬🇧

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikitlearn&logoColor=white)
![F1](https://img.shields.io/badge/F1--Score-~0.85-brightgreen)

## Overview

Predictive model identifying insurance customers likely to purchase vehicle policies (cross-sell), with a systematic comparison of 8 ML algorithms. Winner — SVC with RBF kernel — achieves F1-Score ~0.85 on a heavily imbalanced dataset (handled via SMOTE and class weighting).

End-to-end ML pipeline applicable to Financial Services, Insurance, and enterprise CRM: from feature engineering to model selection with a rigorous, reproducible methodology.

## Results — 8 Algorithm Comparison

| Algorithm | F1-Score | Notes |
|-----------|----------|-------|
| **SVC RBF Kernel** | **~0.85** | **Best performance** |
| Random Forest | ~0.82 | |
| Gradient Boosting | ~0.81 | |
| Logistic Regression | ~0.76 | |
| K-Nearest Neighbors | ~0.74 | |
| Decision Tree | ~0.72 | |
| Naive Bayes | ~0.68 | |
| Linear SVC | ~0.67 | |

## ML Pipeline

```
Raw dataset (imbalanced)  →  EDA + Feature Engineering
    →  Class Imbalance (SMOTE + class_weight)
    →  8 algorithms (cross-validation)  →  SVC RBF selected
    →  F1 · Precision · Recall · ROC-AUC · Confusion Matrix
```

## Setup

```bash
git clone https://github.com/sylver86/09-insurance-cross-sell-prediction-scikit-learn.git
cd 09-insurance-cross-sell-prediction-scikit-learn
pip install -r requirements.txt
jupyter notebook "notebooks/Progetto Machine Learning.ipynb"
```

## Technologies

`Python 3.8+` · `scikit-learn` · `imbalanced-learn` · `pandas` · `NumPy` · `Matplotlib` · `Seaborn`
