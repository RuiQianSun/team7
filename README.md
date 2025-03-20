# Team 7 

## Content

* [Purpose & Overview](#purpose--overview)
* [Goals & Objectives](#goals--objectives)
* [Techniques & Technologies](#techniques--technologies)
* [Key Findings & Instructions](#keyfindings--instructions)
* [Visuals & Credits](#visuals--contacts)

## Purpose & Overview
This project focuses on determing which variables significantly predict the occurence of stroke. Our dataset consists of 11 variables for 5,110 patients, including the variable "stroke" which is 1 if a patient had a stroke or 0 if a patient has not had a stroke. The remaining variables represent a patient's demographic, health, and lifestyle information.

* Age: age of patient
* Gender: gender of patient
* Hypertension: whether the patient has a hypertension
* Heart Disease: whether the patient has heart disease
* Ever Married: whether the patient is married
* Work Type: The type of employment the patient has
* Residence Type: The type of area where the patient resides
* Average Glucose Level: The patient's glucose level
* BMI: the body mass index of the patient
* Smoking Status: whether the individual smokes and to what extent

Business Problem:
We are a data science team working on stroke prevention. Our job is to advise on "which factors significantly predict the occurence of stroke" and "who should receive stroke prevention treatment". 

Industry Context:
In 2021 stroke was one of the top 5 leading causes of death in Canada, responsible for 37 deaths per 100,000 people. Being able to identify predictors of stroke plays a critical role in stroke prevention for the healthcare industry.

1. Early Detection

The ability to predict a stroke before it happens leads to more opportunities to prevent the stroke through lifestyle changes and prevention treatments.
      
2. Targeted Treatment

Identifying which factors predict stroke aides healthcare professional with developing treatments and intervetions for strokes.

## Goals & Objectivs
The project aims to develop an reliable model to predict strokes and identify key features that predict strokes. Our goal is to create a model with high accuracy, precision, recall, and F1 scores.

Change: Due to class imbalance we were unable to achieve a high F1 score, so we are pivoting our model to optimize for recall instead of F1. The value of a high recall model depends on the assumption that false positives (predicting a stroke for a non-stroke patient) are less harmful than false negatives (predicting no stroke for a patient that suffers a stroke).

## Techniques & Technologies

reproducability -> libraries, verisions, programming language, tools, softwares
- pandas
- from sklearn.model_selection import train_test_split
- from sklearn.model_selection import GridSearchCV
- from xgboost import XGBClassifier
- from xgboost import XGBClassifier
- from sklearn.model_selection import cross_val_score, cross_val_predict
- from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, confusion_matrix


Preprocessing (explain rationale)
- Imputation
- Standard Scaling
- Outliers (gender = other, work = child)
- One-Hot-Encoding

Models
- logistic regression (grid seach class_weights)
- decision tress (grid seach class_weights)
- xgboost (class weight vs scale pos weight)?

Techniques & Metrics
- train test split
- grid_search for hyperparameter tuning
- accuracy, precision, recall, F1
- cross validation
- ROC AUC
- feature importance
- SHAP

## Key Findings & Instructions
No setup instructions are required

F1 attempts, accuracy, precision, recall, and f1 for stroke 1 and 0 results
-> subsetting the data

compare the metrics of each model F1 vs Recall, in a table, create an excel
Metrics (f1 vs recall side be side)
- accuracy, precision, recall, F1
- cross validation
- ROC AUC
- feature importance
- SHAP
- explanation in real world terms

key factors, for each variable in our model do we agree or disagree with the SHAP and feature importance, use reasoning and EDA, what is our final answer to "which variable predict strokes"?
- Age

Risks, Unknowns, & Limitations

Limitation: It may not be possible to predict strokes

Limitation: It may not be possible to prevent a stroke even if you can predict it

Unknown: The financial cost of a potential stroke prevention treatment

Unknown: The reliability of the raw data

Unknown: The chronological order of the data (hypertension -> stroke vs stroke -> hypertension)

Risk: Stroke prevention treatment could come with negative side effects or could be dangerous and invasive

## Visuals
EDA visuals, upload PNG files to repo

### Exploratory data anlysis

  #### Class distribution of stroke

  This bar plot shows the distribution of the target variable Stroke across the dataset. As observed, the class distribution is imbalanced, with a larger proportion of individuals who did not have a stroke compared to those who had one.

![alt text](images/distribution.png)

* Histograms of Age and Average Glucose Level and BMI 
![alt text](images/hist.png)

* Scatterplots of Age vs Average Glucose Level and BMI 

![alt text](images/scatterplots.png)

* Pie charts of stroke probability for people with heart disease and hypertension

![alt text](images/hd.png)

![alt text](images/ht.png)

## Credits

* Rui Qian Sun
* Catherine Liang
* Mahbub Khandoker
* Neethila Poddar
* Devangi Vyas