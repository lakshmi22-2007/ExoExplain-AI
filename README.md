# ExoExplain AI 🪐

> **Explainable Machine Learning for Exoplanet Candidate Classification**
> 
> *India High School Exoplanet Data Challenge Entry*

[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](notebook/ExoExplain_AI.ipynb)

---

## 📌 Overview

**ExoExplain AI** is an end-to-end explainable machine learning pipeline designed to automatically classify NASA Kepler Objects of Interest (KOIs) into **Confirmed Exoplanets** vs. **False Positives**. Combining robust ensemble modeling with **SHAP (SHapley Additive exPlanations)** game-theoretic interpretability, ExoExplain AI demystifies complex astrophysical feature interactions—enabling astronomers to verify candidates with confidence.

---

## 📁 Repository Structure

```
ExoExplain-AI/
│
├── data/
│   └── exoplanet.csv                 # NASA Kepler Candidate Dataset
│
├── notebook/
│   └── ExoExplain_AI.ipynb           # Reproducible Jupyter Notebook (17 Sections)
│
├── images/
│   ├── heatmap.png                   # Feature Correlation Matrix
│   ├── roc_curve.png                 # Receiver Operating Characteristic Curve
│   ├── confusion_matrix.png          # Model Evaluation Confusion Matrix
│   ├── feature_importance.png        # Random Forest Gini Feature Importances
│   └── shap_summary.png              # SHAP Beeswarm Interpretability Summary Plot
│
├── reports/
│   └── ExoExplain_AI_Report.pdf      # Detailed Project Report & Documentation
│
├── requirements.txt                  # Required Python Dependencies
├── README.md                         # Project Documentation
└── LICENSE                           # MIT License
```

---

## 📊 Key Results & Evaluation Metrics

Our **Random Forest Classifier** achieved high reliability across validation metrics:

| Metric | Score | Astronomical Significance |
| :--- | :---: | :--- |
| **Accuracy** | **~98%** | High overall classification fidelity across candidate populations. |
| **Precision** | **~97%** | Low rate of false alarm candidate flags. |
| **Recall** | **~98%** | High detection efficiency for true Earth/Jupiter analogue exoplanets. |
| **F1 Score** | **~98%** | Optimal balance between detection sensitivity and precision. |
| **ROC-AUC** | **~0.99** | Exceptional discriminative power across threshold settings. |

---

## 🔍 Explainability Insights (SHAP Analysis)

1. **Signal-to-Noise Ratio (`koi_model_snr`)**: High transit SNR is the strongest positive indicator of confirmed exoplanets.
2. **False Positive Flags (`koi_fpflag_*`)**: Stellar eclipse and centroid offset flags quickly filter binary star background noise.
3. **Planetary Radius (`koi_prad`) & Depth (`koi_depth`)**: Plausible Earth-to-Neptune size profiles distinguish genuine planetary transits from stellar companion eclipses.

---

## 🚀 Quick Start Guide

### 1. Prerequisites & Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/your-username/ExoExplain-AI.git
cd ExoExplain-AI
pip install -r requirements.txt
```

### 2. Running the Notebook

Launch Jupyter Notebook or JupyterLab:

```bash
jupyter notebook notebook/ExoExplain_AI.ipynb
```

---

## 📄 Competition PDF Report

A comprehensive project writeup complete with detailed methodology, astrophysical background, metric breakdowns, and embedded high-res visualizations is available at:
`reports/ExoExplain_AI_Report.pdf`

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
