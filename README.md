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
We are a data science team working with Health Canada on stroke prevention. Our job is to recommend "which areas stroke preventation treatment should address" and "who should receive stroke prevention treatment". 

Industry Context:
The World Health Organization states that stroke is the second leading cause of death worldwide, responsible for ~11% of all deaths. Being able to identify predictors of stroke plays a critical role in stroke prevention for the healthcare industry.

1. Early Detection

The ability to predict a stroke before it happens leads to more opportunities to prevent the stroke through lifestyle changes and prevention treatments.
      
2. Targeted Treatment

Identifying which factors predict stroke aides healthcare professional with developing treatments and intervetions for strokes.

Risks & Unknowns

Risk: It may not be possible to predict strokes

Risk: It may not be possible to prevent a stroke even if you can predict it

Unknown: The cost of a potential stroke prevention treatment

Unknown: The reliability of the raw data

Unknown: The chronological order of the data (hypertension -> stroke vs stroke -> hypertension)

## Goals & Objectivs
The project aims to develop an reliable model to predict strokes and identify key features that predict strokes.

Accuracy >= 80%
Precision >= 70%
Recall >= 70%
F1 >= 70%

Change: Due to class imbalance we were unable to achieve a high F1 score, so we are pivoting to optimize for recall instead of F1.

Recall >= 90%

## Techniques & Technologies
### Preprocessing Tools
- Imputation
- Standard Scaling
- Outliers (gender = other, work = child)
- One-Hot-Encoding

### Models & Methods
- train test split
- logistic regression (grid seach class_weights)
- decision tress (grid seach class_weights)
- xgboost (grid search scale pos weight)

- accuracy, precision, recall, F1
- F1 vs Recall
- ROC AUC
- class weight vs scale pos weight
- feature importance
- SHAP
- grid__search for hyperparameter tuning
- cross validation
- EDA, plots, descriptive statistics

## Key Findings & Instructions
No setup instructions

EDA

F1 -> early attempts
-> subsetting the data

Rationale for the usefulness of high recall, the holistic cost of treatment (false positives) is significantly less than the holistic cost of (false negatives). The overall cost of treatments is feasible.

Recall (final model) -> comparison across models, hyperparameters
-> metrics, ROC AUC, cross validation
-> real world implications
-> SHAP, feature importance

compare the metrics of each model F1 vs Recall, in a table, create an excel

key factors, for each variable in our model do we agree or disagree with the SHAP and feature importance, use reasoning and EDA, what is our final answer to "which variable predict strokes"?

Limitations (move from intro?)

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