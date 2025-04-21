# 🧠 Deep Survival Expert
> Mastering Deep Learning for Survival Analysis – From Statistical Foundations to Cutting-Edge AI Applications

## 🔍 Overview
This repository is a personal learning journey and practical toolkit for deep learning applied to survival analysis. As a Ph.D. candidate in Statistics, my goal is to bridge classical survival models with modern AI techniques to solve real-world time-to-event problems in health, engineering, and finance.

## 📚 Topics Covered
- Survival Analysis: Kaplan-Meier, Cox PH, AFT
- DeepSurv, DeepHit, DeepAFT, Logistic Hazard Models
- Evaluation Metrics: Concordance Index, Brier Score
- Bayesian Deep Survival and Uncertainty Estimation
- Explainability in Survival DL (SHAP, Saliency Maps)
- Real-world Applications: Cancer Survival, Churn Modeling, Asset Depreciation

## 📂 Repo Structure

deep-survival-expert/
├── README.md             # Project overview and instructions
├── environment.yml       # Conda environment file
├── requirements.txt      # (optional) pip-based dependencies
│
├── notebooks/            # Jupyter notebooks for exploration
│   ├── 01_cox_model_basics.ipynb
│   ├── 02_deepsurv_intro.ipynb
│   └── 03_model_comparison.ipynb
│
├── src/                  # Source code for models and utils
│   ├── data_loader.py    # Data preprocessing & loaders
│   ├── models.py         # DeepSurv, DeepHit, etc.
│   ├── train.py          # Training loops
│   ├── eval.py           # Evaluation metrics (C-index, etc.)
│   └── explain.py        # Explainability (e.g., SHAP)
│
├── data/                 # Data access & preprocessing scripts
│   ├── README.md
│   └── seer_preprocessing.py
│
├── projects/             # Real-world projects & case studies
│   ├── 01_cancer_survival/
│   │   ├── notebook.ipynb
│   │   └── report.md
│   └── 02_customer_churn/
│
├── blog/                 # Blog drafts (e.g., Medium)
│   ├── 01-understanding-deepsurv.md
│   └── 02-competing-risk-deephit.md
│
└── docs/                 # Optional: documentation with Sphinx/mkdocs
