# Diabetes_Readmission_Project
Exploratory analysis and predictive modeling of 30-day hospital readmissions for diabetic patients using SQL and R.
Project Overview
This project explores hospital readmission risk among diabetic patients using a combination of SQL-based exploratory data analysis (EDA) and predictive modeling in R. The goal is identify key demographics and clinical factors associated with 30-day readmission, build a logistic regression model to predict readmission risk, and provide actionable insights for healthcare management. All analyses are reproducible, with scripts and data (anonymized) included in the repository. 
Data: 
Souurce: Anonymized diabetes patient dataset from MSK. 
Key Variables: 
Patient_nbr, age, gender, race, total_prior_admissions, num_medications, diabetes_med_flag, high_alc_flag, readmitted (<40 days vs >30/not admitted)
Analysis Workflow
Data Extraction & EDA: Performed in SQLite using SQL queries.
Generated summary tables and basic statistics for all relevant variables.
Feature Engineering:
Created binary flags for readmission within 30 days (readmitted_bin).
Derived clinical features like diabetes medication use and high A1C.
Predictive Modeling:
Logistic regression in R to predict 30-day readmission.
Model evaluation using confusion matrix, ROC curve, and AUC.
Considered class imbalance due to most patients not being readmitted.
Exploratory Analysis Findings
Readmission: ~11% of patients were readmitted within 30 days.
Age: Older patients have slightly higher readmission risk.
Gender: Minimal effect on readmission.
Race: African American, Asian, Hispanic, and Caucasian patients show slightly higher readmission odds.
Clinical Features:
Total prior admissions and number of medications increase readmission risk.
Majority of patients (~77%) are on diabetes medications.
Predictive Modeling Insights
Logistic regression identified the following predictors:
Positive association: total prior admissions, number of medications, age, certain racial groups
Minimal effect: gender
Model performance:
Accuracy: 88.7%
Sensitivity: 99.87% (good at predicting non-readmissions)
Specificity: 0.35% (poor at predicting actual readmissions due to class imbalance)
Implication: Model predicts non-readmissions well but struggles with actual readmissions.
Conclusions
Readmission risk is strongly influenced by prior hospitalizations, number of medications, and age.
Race has a small but significant effect; gender does not meaningfully affect readmission.
Logistic regression performs well for non-readmissions but poorly for predicting actual readmissions due to class imbalance.
Future work: implement class balancing, incorporate additional lab/clinical features, and explore demographic-clinical interactions.
