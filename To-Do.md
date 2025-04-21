# ✅ To-Do List: Deep Survival Analysis Roadmap

📌 This file tracks the progress of your learning, implementation, and content creation.

---

## 📁 00_Foundations
- [x] Write clear README with project vision & roadmap
- [ ] Markdown: `Introduction to Survival Analysis`

---

## 📁 01_Classical_Models

📊 Core Methods
- [ ] 📘 Notebook: Non-parametric Procedures
- [ ] 📘 Notebook: Cox Proportional Hazards Model
- [ ] 📘 Notebook: Parametric Survival Models
- [ ] 📘 Notebook: Accelerated Failure Time (AFT) Models

🧩 Complex Data Structures
- [ ] 📘 Notebook: Frailty Models (Shared & Nested)
- [ ] 📘 Notebook: Recurrent Events Models
- [ ] 📘 Notebook: Competing Risks Analysis
- [ ] 📘 Notebook: Interval-Censored Survival Data
- [ ] 📘 Notebook: Left-Truncation / Delayed Entry

📐 Extensions & Real-World
- [ ] 📘 Notebook: Multi-State Models (Markov & Semi-Markov)
- [ ] 📘 Notebook: Cure Models (Mixture & Non-mixture)
- [ ] 📘 Notebook: Time-Varying Effects in Cox Models
- [ ] 📘 Notebook: Joint Models (Longitudinal + Time-to-Event)

📦 Bayesian & Simulation
- [ ] 📘 Notebook: Bayesian Survival Analysis (w/ PyMC, Stan)
- [ ] 📘 Notebook: Simulation of Survival Data
- [ ] 📘 Notebook: Posterior Predictive Survival Curves
- [ ] 📘 Notebook: Sensitivity Analysis with Priors

🧪 Diagnostics & Model Fit
- [ ] 📘 Notebook: Proportional Hazards Assumption Checks
- [ ] 📘 Notebook: Goodness-of-Fit for AFT & Parametric Models
- [ ] 📘 Notebook: Cox-Snell Residuals, Martingale Residuals
- [ ] 📘 Notebook: Model Selection — AIC, BIC, Cross-Validation

📈 Evaluation & Validation
- [ ] 📘 Notebook: Concordance Index, Harrell’s C
- [ ] 📘 Notebook: Time-dependent AUC / ROC
- [ ] 📘 Notebook: Brier Score & Integrated Brier Score
- [ ] 📘 Notebook: Calibration Curves & Belts
- [ ] 📘 Notebook: External Validation (Train/Test Split)

---

## 📁 02_Deep_Models

🌐 Foundational Models
- [ ] 📘 Notebook: DeepSurv (PyTorch)
  - Architecture, loss (Negative Partial Log-Likelihood)
  - Handling censored data
  - Custom layer for baseline hazard (optional)

- [ ] 📘 Notebook: Cox-Time & Cox-CC (from pycox)
  - Time transformation concept
  - Differences from DeepSurv
  - Use on real-world dataset (e.g. SUPPORT / METABRIC)

- [ ] 📘 Notebook: DeepHit
  - Multi-task classification framework
  - Competing risks support
  - Ranking + log-likelihood losses
  - Evaluation: top-k accuracy, CIF curves

- [ ] 📘 Notebook: Neural Multi-Task Logistic Regression (Neural-MTLR)
  - Survival function as sum of logistic outputs
  - Smooth hazard functions
  - Calibration evaluation

- [ ] 📘 Notebook: N-MTLR vs DeepSurv: When to Use What
  - Non-proportional hazards?
  - Survival function vs hazard modeling

🧪 Evaluation
- [ ] 📘 Notebook: Model Performance Metrics
  - Concordance index (C-index, time-dependent)
  - Brier score & Integrated Brier Score
  - Time-dependent AUC
  - Calibration curves
  - Log-loss and ranking loss (for DeepHit)

📝 Theory & Assumptions
- [ ] 📘 Notebook: Loss Functions Overview
  - Partial log-likelihood, CRPS, log-loss, hinge loss
  - How loss functions relate to censoring

- [ ] 📘 Notebook: Writeups per Method (Markdown or Jupyter markdown cells)
  - Assumptions of each model
  - Architectural design
  - Mathematical formulation
  - Loss derivation
  - Implementation notes

🔁 Reproducibility
- [ ] 📘 Notebook: Reproducing Published Deep Survival Papers
  - E.g. "DeepHit" on METABRIC or SEER
  - E.g. "Cox-Time" on SUPPORT

📦 Extras (Advanced)
- [ ] 📘 Notebook: Dynamic-DeepHit (for time-dependent covariates)
- [ ] 📘 Notebook: SurvTRACE (transformer-based survival)
- [ ] 📘 Notebook: Transfer Learning for Survival Models
- [ ] 📘 Notebook: Federated Survival Analysis


---

## 📁 03_Case_Studies

### 🏭 Reliability Engineering
- [ ] 📘 Case Study: **Reliability of Industrial Systems**
  - Objective: Predict the lifetime and failure risk of a system (e.g., pumps, engines)
  - Data: Simulated reliability data (e.g., Weibull, exponential distributions)
  - Models: AFT, DeepSurv, Neural-MTLR
  - Metrics: C-index, Brier score, calibration plots
  - Visualizations: Hazard functions, lifetime distribution
  - Discussion: Differences between classical and deep models in reliability context

- [ ] 📘 Case Study: **Maintenance and Failure Prediction in Manufacturing**
  - Objective: Predict system failure times and recommend preventive maintenance schedules
  - Data: Failure data, component life cycles (real-world or simulated)
  - Models: Cox-Time, DeepSurv, Dynamic DeepHit
  - Metrics: Time-dependent AUC, Brier score, survival curves for maintenance intervals
  - Visualizations: Maintenance window optimization, survival and failure probabilities over time

### 🏥 Medical Studies
- [ ] 📘 Case Study: **Heart Disease Survival Prediction**
  - Objective: Predict patient survival time after heart surgery or heart disease diagnosis
  - Data: Clinical dataset (e.g., Cleveland Heart Disease dataset)
  - Models: Cox Proportional Hazards, DeepSurv, Neural-MTLR
  - Metrics: Concordance index (C-index), Brier score, survival curves by feature (age, cholesterol)
  - Visualizations: Kaplan-Meier curves by risk factor, time-dependent AUC

- [ ] 📘 Case Study: **Cancer Treatment Effectiveness (METABRIC)**
  - Objective: Predict breast cancer relapse or survival based on treatment type
  - Data: METABRIC dataset (clinical and genomic data)
  - Models: DeepSurv, DeepHit, Cox-Time
  - Metrics: C-index, Log-likelihood, time-dependent AUC, calibration
  - Visualizations: Hazard ratios, risk group stratification

- [ ] 📘 Case Study: **Diabetes Progression Prediction**
  - Objective: Predict the time to diabetes onset from various biomarkers
  - Data: Medical records, biomarkers (e.g., glucose levels, age)
  - Models: AFT, DeepSurv, Neural-MTLR
  - Metrics: Survival curves, calibration plots, C-index
  - Visualizations: Feature importance, risk groups stratification

### 💼 Actuarial Sciences
- [ ] 📘 Case Study: **Insurance Claim Prediction**
  - Objective: Predict the time to the next insurance claim (e.g., auto, health insurance)
  - Data: Historical claims data (e.g., age, medical history, claim frequency)
  - Models: Cox Proportional Hazards, DeepSurv
  - Metrics: C-index, AIC/BIC for model selection, Brier score
  - Visualizations: Cumulative incidence function (CIF), survival probability over time

- [ ] 📘 Case Study: **Pension Fund Liability Modeling**
  - Objective: Predict the time to pension fund depletion based on participant life expectancy
  - Data: Actuarial tables, demographic data (e.g., age, mortality rate)
  - Models: Parametric survival models, DeepSurv, Neural-MTLR
  - Metrics: Calibration curves, survival curves by cohort, Brier score
  - Visualizations: Cohort-wise risk and lifetime estimates

- [ ] 📘 Case Study: **Risk Analysis for Catastrophic Events**
  - Objective: Predict time to catastrophic events (e.g., natural disasters, major economic crises)
  - Data: Historical event data (e.g., earthquake magnitudes, insurance claims after disasters)
  - Models: DeepHit, AFT models
  - Metrics: C-index, time-dependent AUC, survival curve comparisons by risk group
  - Visualizations: Risk scenarios, tail-end risks, hazard function for extreme events

### 🧑‍🔬 Insight & Communication
- [ ] 📘 Visualizations + Interpretation Notebook
  - Key Visuals: Kaplan-Meier, AFT-based survival curves, hazard ratios, calibration plots
  - Interpretation: Explain findings with industry context (reliability, healthcare, insurance)
  - Use advanced explainability techniques (SHAP, Integrated Gradients for neural models)

✍️ Science Communication
- [ ] 📝 Post: *“How I Applied Deep Survival Models to Real-World Data”*
  - Blog-style write-up: Problem, method selection, modeling approach, and final results
  - Discussion: How the models improve upon traditional methods in each field (reliability, medical, actuarial)
  - Include visuals + code snippets + GitHub link


---

## 📁 04_Portfolio_Project

### 🗂️ Project Overview
- [ ] **End-to-End Project Folder**
  - **Code**: Full project pipeline (data preprocessing, model development, evaluation)
  - **Data**: Cleaned and processed datasets (raw + final dataset versions)
  - **Slides**: Key findings, methodologies, and insights for presentation
  - **ReadMe**: A high-level overview of the project, including how to run the code
  - Folder Structure:
    ```bash
    04_Portfolio_Project/
    ┣ code/
    ┣ data/
    ┣ slides/
    ┣ results/
    ┣ portfolio.md
    ┗ README.md
    ```
  
- [ ] **`portfolio.md`**: Executive Summary
  - A concise overview of the problem, methodology, and results.
  - Target Audience: Hiring managers, industry professionals, and potential collaborators.
  - Structure: 
    1. **Problem Statement**: Why is this important in your field (reliability, medical, actuarial)?
    2. **Methodology**: Classical vs. Deep Learning methods used.
    3. **Results**: Key metrics and model performance (e.g., C-index, AUC).
    4. **Insights**: How your model can be applied in real-world situations.
    5. **Conclusion**: What are the next steps, and how can the model be further improved?

- [ ] **Streamlit Demo or Jupyter Dashboard (Optional)**
  - Create an interactive demo or dashboard for visualizing results and exploring the model's predictions.
  - **Streamlit Example**: Allow users to upload data, see predictions, and visualize survival curves or hazard functions.
  - **Jupyter Dashboard Example**: Organize notebooks in an interactive form to present your work and findings with inline visualization.

- [ ] **Add Results to Resume**
  - Add the project to your resume as a standalone item:
    - Title: *Deep Learning for Survival Analysis on [Dataset/Problem]*
    - Technologies: Python, PyTorch/TensorFlow, Streamlit/Jupyter, [any specific libraries like Lifelines, Scikit-Survival]
    - Bullet points: Briefly mention the impact of your project, methodologies used, and the main outcomes (e.g., improved model accuracy, successful prediction of survival times).

---

📆 Progress Check: Update weekly, post progress, and celebrate milestones!
