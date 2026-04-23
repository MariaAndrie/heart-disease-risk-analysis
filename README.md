# Heart Disease Risk Analysis

A portfolio project focused on exploratory data analysis, baseline classification, and Tableau dashboarding for heart disease risk analysis using patient clinical data.

## Project Overview

This project explores a clinical dataset to identify factors associated with heart disease and to build a baseline machine learning model for classification.

The workflow includes:
- data inspection and cleaning
- exploratory data analysis (EDA)
- logistic regression modeling
- Tableau dashboarding

The goal is to understand which patient attributes are most associated with heart disease status and present the findings in a clear, visual format.

## Problem Statement

Cardiovascular disease is one of the leading health concerns worldwide. Identifying patterns in patient data can help better understand risk factors associated with heart disease.

In this project, I analyzed patient-level clinical data to:
- explore key variables related to heart disease
- identify patterns and relationships between features
- build a baseline classification model
- visualize differences between diseased and healthy patients

## Dataset

The dataset contains 303 patient records and 14 attributes, including demographic and clinical variables.

### Features

- `age` — age of the patient  
- `sex` — gender  
- `cp` — chest pain type  
- `trestbps` — resting blood pressure  
- `chol` — cholesterol level  
- `fbs` — fasting blood sugar  
- `restecg` — resting ECG results  
- `thalach` — maximum heart rate achieved  
- `exang` — exercise-induced angina  
- `oldpeak` — ST depression induced by exercise  
- `slope` — slope of the peak exercise ST segment  
- `ca` — number of major vessels colored by fluoroscopy  
- `thal` — thalassemia category  
- `target` — heart disease status (0 = Diseased, 1 = Healthy)  

## Project Workflow

### 1. Data Inspection
- checked dataset structure and data types  
- verified missing values  
- checked for duplicates  
- reviewed summary statistics  

### 2. Exploratory Data Analysis
- analyzed categorical variables using count plots  
- explored distributions of key numerical variables  
- compared variables across target groups  
- used boxplots to identify differences between Diseased and Healthy patients  
- built pairplots to explore relationships between features  

### 3. Modeling
- split data into training and test sets  
- trained a Logistic Regression model  
- generated predictions on test data  
- evaluated results using a confusion matrix  

### 4. Dashboarding
- created Tableau dashboards to compare Diseased vs. Healthy patients  
- visualized key variables and their relationships  
- highlighted patterns for easier interpretation  

## Key Insights

- Male patients show a higher proportion of heart disease compared to female patients  
- Exercise-induced angina (`exang`) is strongly associated with the Diseased group  
- Higher values of `ca` are linked to increased presence of heart disease  
- Diseased patients tend to have higher `oldpeak` values  
- Diseased patients generally have lower `thalach` (max heart rate)  
- Cholesterol alone does not clearly separate Diseased and Healthy groups  
- The most influential features in the model include `sex`, `exang`, `thal`, `ca`, and `oldpeak`  

## Model Performance

Confusion matrix:

```
[[25, 4],
[ 3, 29]]
```

Approximate accuracy: **88.5%**

The model performs well as a baseline classifier, with relatively low misclassification on the test set.

## Tableau Dashboards

The dashboards focus on comparing Diseased and Healthy patients and identifying key patterns across variables.

Included:
- categorical comparisons (gender, thal, exang, ca)  
- numerical comparisons (age, cholesterol, oldpeak)  
- scatter plots for feature relationships  

## Repository Structure

```
heart-disease-risk-analysis/
├── README.md
├── requirements.txt
├── data/
│ ├── data.xlsx
│ └── variable_description.xlsx
├── notebooks/
│ └── heart_disease_analysis.ipynb
├── dashboards/
│ ├── tableau_dashboard_1.png
│ └── tableau_dashboard_2.png

```

## Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- scikit-learn  
- Tableau  

## Future Improvements

- add preprocessing pipeline (scaling, feature engineering)  
- compare multiple models  
- include additional evaluation metrics (ROC-AUC, precision, recall)  
- improve feature interpretation  
- publish interactive Tableau dashboard  

## Disclaimer

This project is for educational and portfolio purposes only.  
It is not intended for medical or clinical use.

## Author

Portfolio project demonstrating:
- data analysis  
- visualization  
- machine learning basics  
- dashboarding  
