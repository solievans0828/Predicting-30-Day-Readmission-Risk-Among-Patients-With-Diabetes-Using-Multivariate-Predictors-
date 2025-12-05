# Predicting-30-Day-Readmission-Risk-Among-Patients-With-Diabetes-Using-Multivariate-Predictors-

### Authors

Soli Evans
Abhimaan Mayadam
#  https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008

---

## Project Overview

This repository contains the full analytical workflow, report, presentation, and dataset used to examine predictors of **30-day hospital readmission among diabetic patients**. The project uses a large, multicenter dataset to explore demographic, clinical, and utilization factors contributing to readmission risk, and evaluates both logistic regression and machine-learning models.

The objective of this work was to:

* Identify key predictors of short-term readmission
* Build and evaluate statistical and machine-learning models
* Compare model performance using ROC curves, AUC values, and classification metrics
* Translate findings into actionable insights for healthcare quality improvement

Comprehensive details of the methodology and findings can be found in the **Final Project Report**  and the **Final Presentation** . Supporting code and workflow documentation appear in the **Appendix** .

---

## Repository Structure

```
project-folder
├── README.md
├── Final Project Report HI2251.pdf
├── Final Project Report HI 2251 Appendix.pdf
├── HI2251 Final Presentation.pdf
```

---

## Dataset

**UCI Diabetes 130-US Hospitals Dataset**
Cleaned version used in this project: `diabetic_data_na_removed.csv`

The dataset contains over **100,000 inpatient encounters** for patients with diabetes across 130 hospitals, covering demographic data, clinical variables, utilization measures, diagnoses, treatment indicators, and readmission outcomes. A binary outcome variable was created to indicate **whether a patient was readmitted within 30 days**.

The dataset source is documented in the report and presentation under Works Cited and originated from the UCI Machine Learning Repository.

---

## Methods Summary

### 1. Data Cleaning

* Removal of invalid or missing values
* Conversion of age ranges to numeric midpoints
* Encoding of categorical variables
* Selection of clinically relevant predictors

R and Python were used for initial preprocessing steps, as detailed in Appendix A and B .

### 2. Modeling

Models examined:

* Logistic Regression (baseline, interpretable model)
* Random Forest
* Gradient Boosting (best performing model)

Orange Data Mining was used to create the modeling workflow and generate ROC visualizations.

### 3. Evaluation Metrics

* ROC Curves for both Target 0 and Target 1
* AUC
* F1 Score
* Precision, Recall
* MCC (Matthew’s Correlation Coefficient)

Model performance comparisons can be found in the Results and Discussion sections of the Final Report .

---

## Key Findings

### Descriptive Insights

* Majority of hospital encounters involve adults aged **60–80 years**.
* Gender distribution shows slightly more female than male encounters.
* Racial distribution is highly imbalanced, with ~74 percent of patients identified as Caucasian.

### Predictive Modeling Results

* **Inpatient visits** were the strongest predictor of readmission (OR ≈ 1.32).
* **Emergency visits** had a smaller but significant impact.
* Demographic variables such as **age** and **gender** contributed minimally.
* Gradient Boosting achieved the **highest AUC (~0.674)**.
* Logistic Regression performed moderately (**AUC ~0.640**), while Random Forest performed slightly worse.

### Interpretation

Models suggest that prior utilization history is more predictive of readmission than demographic or clinical measures alone. Machine-learning methods showed moderate improvement over logistic regression, likely due to their ability to capture nonlinear patterns.

More details appear in Section 4–6 of the Final Report .

---

## Files Included

### 1. **Final Project Report HI2251.pdf**

A complete written analysis covering the introduction, dataset description, methodology, results, discussion, and conclusions. Contains figures, ROC curves, and tables summarizing model performance.

### 2. **Final Project Report HI 2251 Appendix.pdf**

Contains:

* Python code used for feature engineering and logistic regression modeling
* Notes on R, Python, and Orange
* Visual figures, workflow diagrams, and ROC screenshots
  Cited as: 

### 3. **HI2251 Final Presentation.pdf**

Slide deck summarizing the project for oral defense, including:

* Background and motivation
* Dataset overview
* Visualizations
* Modeling workflow
* ROC and AUC results
* Limitations and future directions

---

## How to Reproduce the Analysis
1. Load dataset from link and remove na values
2. Refer to Appendix A for the full environment setup and modeling code.
3. Use the Orange workflow (documented in Appendix C) to reproduce machine-learning pipelines.
4. Replicate visualizations and model comparisons using Python or Orange.

---

## Citation

If referencing this work, cite the Final Project Report using standard academic formatting. Details and references are included at the end of the Report PDF.

