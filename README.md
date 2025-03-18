# Team 7 

## Content

* [Overview](#overview)
* [Goals](#goals)
* [Techniques](#techniques)
    + [Models](#models)
* [Key Findings](#findings)
* [Visuals](#visuals)
* [Contacts](#contacts)

## Overview 
This repository focuses on solving a classification problem -  **A Stroke Prediction**. According to the World Health Organization (WHO), stroke is the second leading cause of death worldwide. In this project, we train multiple machine learning models on a relevant dataset to predict the likelihood of stroke. The goal is to identify key features that influence stroke risk and develop an accurate predictive model for better healthcare outcomes.

The Kaggle stroke dataset consists of a collection of data from 5110 individuals. Each record represents an individual’s demographic, health, and lifestyle information, along with whether they had a stroke or not. Key variables in the dataset include:

* Age: The age of the individual.
* Gender: The gender of the individual.
* Hypertension: Whether the individual has a history of hypertension.
* Heart Disease: Whether the individual has a history of heart disease.
* Ever Married: Whether the individual is married or not.
* Work Type: The type of employment the individual has (e.g., private, self-employed, government, etc.).
* Residence Type: The type of area where the individual resides (urban or rural).
* Average Glucose Level: The individual’s glucose level (indicating potential metabolic issues).

* BMI: The body mass index, a key indicator of weight-related health risks.
* Smoking Status: Whether the individual smokes and the extent of their smoking habits.

### Industry Context and Relevance of Stroke Data

The healthcare and medical industry plays a critical role in addressing stroke prevention, treatment, and rehabilitation.  Understanding stroke risk factors through this dataset can help us in several ways:

1. Early Diagnosis and Risk Prediction: 
      Stroke prediction models can help healthcare providers assess an individual’s risk level before a stroke occurs. Machine learning and predictive analytics can predict the likelihood of a stroke based on personal health data, such as age, BMI, blood pressure, and lifestyle factors.Early diagnosis and intervention can significantly reduce the mortality rate and long-term disability caused by strokes.
      
2. Improved Healthcare Services:
Identifying the prevalence of stroke risk factors in specific regions (urban or rural) can lead to more effective allocation of healthcare resources, including specialized stroke centers, rehabilitation services, and preventative care.

3. Targeted Preventative Programs: This dataset can help to identify the most common risk factors associated with stroke. For instance, if smoking or high glucose levels are identified as major contributors to stroke risk, tailored public health campaigns can focus on educating individuals about the dangers of smoking and the importance of controlling blood sugar levels.

## Goals
 To identify key features that influence stroke risk and develop an accurate predictive model for better healthcare outcomes

## Techniques
Before preceedings to the training the model, we understand the data and perform the preprocessing. During the pre-processing, we update the missing numeric values with its mean, categorize the non-numeric values, and standardize the numeric ones.


### Models

## Key Findings

## Visuals

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

## Contacts

* Rui Qian Sun
* Catherine Liang
* Mahbub Khandoker
* Neethila Poddar
* Devangi Vyas