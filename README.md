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
