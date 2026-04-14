# ADSP 31017 – Machine Learning I
## Final Project: Predicting Shipment Delivery Delays

**University of Chicago**  
**Instructor:** Gizem Agar  
**Term:** Winter 2026  

---

## Team Members

G5:   
- Daniel Babnigg  
- Aren Mizuno 
- Emily Xue
-  Hoon Yum  

---

## Deliverables

- `final_notebook.ipynb` – Full analysis, modeling, and evaluation  
- `final_notebook.html` – Exported notebook for presentation  
- `final_presentation.pptx` – Final presentation slides  
- `final_report.docx` – Written technical report  
- `final_recording.mp4` – Project walkthrough and presentation  

---

## Overview

This project focuses on predicting shipment delivery delays using machine learning models applied to real-world logistics data. The goal is to identify key drivers of delivery time deviations and provide actionable insights to improve operational efficiency and reduce delays.

---

## Data

The dataset contains **32,065 shipment-level observations** from a logistics network (LogistiCorp) spanning **2021–2024**.

Each observation represents a single shipment and includes:
- Operational metrics (traffic congestion, costs, inventory levels)  
- Driver-related features (behavior score, fatigue)  
- Environmental factors (weather conditions)  
- Route and supplier characteristics  

**Target Variable:**
- `delivery_time_deviation` (in hours)  
  - Negative → early  
  - 0 → on time  
  - Positive → delayed  

---

## Methodology

- **Data preprocessing:**
  - Removed missing values (~5.8%) after confirming minimal impact  
  - One-hot encoded categorical variables (e.g., day of week)  
  - Standardized features for linear/regularized models  

- **Feature engineering:**
  - `day_of_week` from timestamp  
  - `driver_risk_score` combining behavior and fatigue  

- **Modeling approach:**
  - Linear Regression  
  - Ridge, Lasso, Elastic Net  
  - Random Forest  
  - Gradient Boosting / XGBoost  
  - Support Vector Regression (SVR)  
  - Polynomial Ridge (nonlinear extension)  

- **Validation:**
  - 80/20 train-test split  
  - 5-fold cross-validation  
  - Grid search for hyperparameter tuning  

- **Evaluation metrics:**
  - RMSE (primary)  
  - MAE  
  - R²  

---

## Key Findings

- Linear Regression performed best overall with **lowest RMSE (~3.37 hours)**  
- Model performance across methods was relatively similar (R² ≈ 0.45)  
- Key drivers of delays include:
  - Traffic congestion  
  - Driver behavior  
  - Weather severity  
- Operational and environmental factors have a stronger impact than supplier-related variables  

---

## Business Impact

- Estimated **$97M annual penalty exposure** from delayed shipments  
- Model identifies “intervention zone” shipments where delays can be prevented  
- With a 50% intervention success rate:
  - ~$16.5M gross savings  
  - ~$13.9M net annual savings  

---

## Skills & Concepts Demonstrated

- Supervised machine learning (regression models)  
- Feature engineering and selection  
- Model evaluation and cross-validation  
- Interpretable modeling (Linear Regression)  
- Tree-based models and nonlinear methods  
- Business translation of ML outputs (financial impact)  
- End-to-end ML pipeline development  

---
