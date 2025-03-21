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
### Exploratory data analysis
#### Class distribution of stroke

  This bar plot shows the distribution of the target variable 'Stroke' across the dataset. As observed, the class distribution is highly imbalanced, where out of 5110 individuals, 4861 (95.13%) are non-stroke and 249 (4.87%) are susceptible to stroke.

![alt text](images/distribution.png)

#### Plots of categorical features by stroke status:

![alt text](images/categorical_col.png)

* Comparing stroke rates between genders: 

    It is observed that the risk of stroke in both males and females are almost same - 4.71% fpr females and 5.11% for males. This observation matches the feature importance and SHAP outcomes that gender is not a significant predictor for strokes.

* Stroke likelihood based on marital status:

    From the plots it is observed that among the married individuals 6.56% and among unmarried ones 1.65% had a stroke. This shows that, in the dataset, the proportion of individuals who had a stroke is higher among married individuals than unmarried individuals.
    
    Considering all patients who had stroke, 88.35% of them are married and 11.84% are unmarried, as demonstrated in the pie chart. This indicates a correlation between marital status and stroke probability, with stroke rate being significantly higher among married individuals compared to unmarried ones. The feature importance of marital status is 0, which indicates that while this may be statistically significant, it is not a strong predictor for strokes.

    ![alt text](images/em.png)

* Proportion of stroke by residence type:

  From the plots it is observed that 54.22% of the individuals who had a stroke are from urban areas and 45.78% from rural areas. The urban population has a slightly higher proportion of stroke cases compared to the rural population, but the difference is not very large. This might indicate that other factors (such as age, preexisting health conditions, etc.) could be contributing to stroke cases in urban areas. The results align with feature importance scores for residence type.

* Proportion of stroke by work type:

  The distribution of stroke cases based on work type shows that among the patients who suffered a stroke, 59.84% work private, 26.10% are self-employed, 13.25% are government job holders and the other categories 'children' and 'never worked' are negligible. It is observed that the 'private' sector has the largest proportion of stroke cases, 'self-employed' group also makes up a substantial portion, while 'Govt_job' has a smaller contribution. However, the feature importance and SHAP values show that the self-employed category is a stronger predictor of strokes compared to the other work categories.

  ![alt text](images/worktype.png)

* Stroke probability based on smoking status:

  From the smoking status distribution it is observed that among the patients who suffered a stroke, 36.14%  never smoked, 28.11% formerly smoked, 18.88% have unknown smoking status and 16.87% currently smokes. The largest proportion of stroke cases come from people who have never smoked, which might be surprising but the combined proportion of stroke patients who previously smoked or currently smokes is quite significant. The feature importance of smoking status is negligible which shows that this is not a good predictor of strokes.

From the exploratory data analysis of all the categorical features and comparing them to the feature importance scores and SHAP values, it is observed  that the self-employed work type is the only significant predictor of stroke while marital status has significant statistical significance.


  ![alt text](images/smoke.png)




Risks, Unknowns, & Limitations

Limitation: It may not be possible to predict strokes

Limitation: It may not be possible to prevent a stroke even if you can predict it

Unknown: The financial cost of a potential stroke prevention treatment

Unknown: The reliability of the raw data

Unknown: The chronological order of the data (hypertension -> stroke vs stroke -> hypertension)

Risk: Stroke prevention treatment could come with negative side effects or could be dangerous and invasive

## Visuals

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