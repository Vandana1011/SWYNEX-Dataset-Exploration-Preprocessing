# SWYNEX-Dataset-Exploration-Preprocessing
# SkyShield — Aviation Wildlife Strike Analysis

## Project Overview
SkyShield explores real-world aviation wildlife strike reports using data from the Federal Aviation Administration (FAA). The project focuses on understanding wildlife strike patterns and preparing the dataset for future machine learning experiments.

## Dataset
- **Source:** [FAA Wildlife Strike Database](https://www.faa.gov/airports/airport_safety/wildlife)
- **Format:** Excel / tabular data
- **Data type:** Real-world reported aviation wildlife strike incidents

## Work Completed
- Explored dataset structure, columns, and data types.
- Analysed missing values and duplicate records.
- Explored incident patterns by year, month, weekday, airport, species, flight phase, and time of day.
- Investigated damage categories and class imbalance.
- Created date-based features.
- Selected relevant features for future damage classification.
- Prepared numerical and categorical preprocessing pipelines using median imputation, categorical encoding, and a train-test split.

## Tools Used
Python, Pandas, Matplotlib, Jupyter Notebook, Scikit-learn.

## Important Limitations
Reported incident counts do not directly represent strike probability because flight-traffic exposure data is not included. Damage labels are imbalanced, and missing damage labels were excluded from the supervised modelling dataset rather than assumed to mean no damage.

## Future Scope
- Develop and evaluate a wildlife-strike damage classification model.
- Explore airport and seasonal risk patterns.
- Build a dashboard for interactive analysis.

## Internship
Completed as part of the SWYNEX Task 1 dataset exploration and preprocessing activity.

# SWYNEX Task 2 — Machine Learning Model Training and Evaluation

## Project Overview

This project focuses on training and evaluating machine learning models using the real-world FAA Wildlife Strike Database as part of Task 2 of the SWYNEX internship.

The project uses the SkyShield aviation safety concept to explore whether wildlife strike damage levels can be predicted from incident-related features.

## Objectives

- Prepare the cleaned dataset for machine learning.
- Select relevant features and define the target variable.
- Train at least two machine learning classification models.
- Evaluate model performance using appropriate metrics.
- Compare the models and explain their relative performance.

## Dataset

**Source:** FAA Wildlife Strike Database

The dataset contains aviation wildlife strike incident information, including airport, aircraft, operator, phase of flight, wildlife species, incident timing, and damage-related fields.

## Machine Learning Models

### 1. Logistic Regression
Used as a baseline classification model.

### 2. Random Forest Classifier
Used to model potentially nonlinear relationships between incident characteristics and damage levels.

## Data Preparation

- Removed records with missing target values.
- Excluded incident identifiers and outcome-related fields from model predictors.
- Handled missing feature values using imputation.
- Encoded categorical variables using One-Hot Encoding.
- Scaled numerical features for Logistic Regression.
- Split the data into training and testing sets using stratified sampling.

## Evaluation Metrics

Both models were evaluated using:

- Accuracy
- Macro Precision
- Macro Recall
- Macro F1-score
- Classification Report
- Confusion Matrix

Macro F1-score was used to compare performance across damage categories, including less frequent classes.

## Model Comparison

Logistic Regression and Random Forest were evaluated on the same held-out test set. The model with the higher macro F1-score was selected as the leading candidate, while class-wise precision, recall, and confusion matrices were also considered.

Actual evaluation results are documented in `SkyShield_Model_Comparison.csv` and `SkyShield_Best_Model_Report.csv`.

## Files

- `SkyShield_Task2_Model_Training_Evaluation.ipynb` — Model training and evaluation notebook.
- `SkyShield_Model_Comparison.csv` — Comparison of evaluation metrics.
- `SkyShield_Best_Model_Report.csv` — Detailed classification report for the selected model.
- `SkyShield_Best_Model.joblib` — Saved trained model.
- `SkyShield_Cleaned_Data.csv` — Prepared dataset used for training, if included.

## Technologies Used

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Jupyter Notebook.

## Conclusion

This task demonstrates a machine learning workflow for aviation wildlife strike damage-level classification. The models were compared using multiple evaluation metrics to identify a promising candidate for further investigation.

The results are experimental and should not be interpreted as validated predictions for operational aviation safety decisions.

## Internship

Completed as part of **Task 2 — Machine Learning Model Training and Evaluation** at **SWYNEX Technologies**.

# SkyShield — Model Improvement and Validation

## SWYNEX Internship — Task 3

### Project Overview
SkyShield analyzes real-world aviation wildlife strike data to explore incident characteristics and predict wildlife strike damage levels using machine learning.

### Objective
Improve and validate the baseline machine learning model through hyperparameter tuning and cross-validation.

### Dataset
- **Records:** 358,433 rows in the cleaned dataset
- **Features:** 14 input features used for modeling
- **Target:** `DAMAGE_LEVEL`
- Missing target labels were excluded from model training.

### Methodology
- Numerical feature imputation and standardization
- Categorical feature imputation and one-hot encoding
- Logistic Regression baseline model
- GridSearchCV with 3-fold Stratified Cross-Validation
- Macro F1-score used for model selection due to class imbalance

### Model Performance

| Metric | Task 2 Baseline | Task 3 Tuned |
|---|---:|---:|
| Accuracy | 0.6669 | 0.6622 |
| Macro Precision | 0.2710 | 0.2723 |
| Macro Recall | 0.4327 | 0.4527 |
| Macro F1-score | 0.2821 | 0.2837 |

### Findings
The tuned model achieved a small Macro F1 improvement from 0.2821 to 0.2837. Macro Recall improved from 0.4327 to 0.4527, while accuracy decreased slightly.

The results suggest modest improvement in identifying different damage classes. Further feature engineering, alternative models, and class-imbalance experiments could improve performance.

### Limitations
The target classes are imbalanced, and the model's overall performance remains limited. The model is intended for learning and analysis and is not validated for operational aviation safety decisions.

### Files
- `SkyShield_Task3_Model_Improvement.ipynb` — Model tuning, validation, evaluation, and findings.

### Tools and Technologies
Python, Pandas, NumPy, Scikit-learn, Jupyter Notebook, Matplotlib.

### Internship
Completed as part of the SWYNEX internship Task 3.


