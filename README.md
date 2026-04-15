# ADSP 31017 – Machine Learning I
## Final Project: Predicting Shipment Delivery Delays

**University of Chicago**  
**Instructor:** Gizem Agar  
**Term:** Winter 2026  

**Team Members:** G5  
- Daniel Babnigg  
- Aren Mizuno  
- Emily Xue  
- Hoon Yum  

---

## Overview

This repository contains my final project for *ADSP 31017: Machine Learning I*, a course focused on supervised learning methods, model evaluation, and practical machine learning workflows.

The course emphasized building predictive models, performing feature engineering, validating model performance, and translating results into actionable business insights.

---

## Final Project

**Description:**  
This project focuses on predicting shipment delivery delays using machine learning models applied to real-world logistics data. The goal is to identify key drivers of delivery time deviations and provide actionable insights to improve operational efficiency and reduce delays.

The dataset contains **32,065 shipment-level observations** from a logistics network spanning **2021–2024**, with features including operational metrics, driver behavior, environmental conditions, and route characteristics.

**Target Variable:**
- `delivery_time_deviation` (in hours)  
  - Negative → early  
  - 0 → on time  
  - Positive → delayed  

---

### Methodology

- **Data preprocessing:**
  - Removed missing values (~5.8%) after confirming minimal impact  
  - One-hot encoded categorical variables  
  - Standardized features for linear and regularized models  

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

### Key Findings

- Linear Regression performed best overall with **lowest RMSE (~3.37 hours)**  
- Model performance across methods was relatively similar (R² ≈ 0.45)  
- Key drivers of delays include:
  - Traffic congestion  
  - Driver behavior  
  - Weather severity  
- Operational and environmental factors have a stronger impact than supplier-related variables  

---

### Business Impact

- Estimated **$97M annual penalty exposure** from delayed shipments  
- Model identifies high-risk shipments for targeted intervention  
- With a 50% intervention success rate:
  - ~$16.5M gross savings  
  - ~$13.9M net annual savings  

---

### Project Deliverables

- `final_notebook.ipynb`  
  → Full analysis, modeling, and evaluation  

- `final_notebook.html`  
  → Exported notebook for presentation  

- `final_presentation.pptx`  
  → Final presentation slides  

- `final_report.docx`  
  → Written technical report  

- `final_recording.mp4`  
  → Project walkthrough and presentation  

---

## Skills & Concepts Demonstrated

- Supervised machine learning (regression models)  
- Feature engineering and preprocessing  
- Model evaluation and cross-validation  
- Regularization techniques (Ridge, Lasso, Elastic Net)  
- Tree-based and nonlinear models  
- Hyperparameter tuning (Grid Search)  
- Translating ML outputs into business insights  
- End-to-end machine learning pipeline development  

---
