# Stroke Risk Analysis with Mental Health Proxy
## Background
Stroke is one of the leading causes of death and disability worldwide. While traditional risk factors such as age and cardiovascular conditions are well studied, the role of mental health remains less explored.

Understanding how psychological and lifestyle factors influence stroke risk can support early intervention and improve healthcare outcomes.

---

## Objective
This project aims to investigate whether mental health-related factors (approximated using smoking behavior) are associated with stroke risk and whether they improve predictive modelling.

---


## Project Overview

This project explores the relationship between mental health (approximated by smoking behavior) and stroke risk using a healthcare dataset.

The goal is to understand how psychological and lifestyle factors contribute to stroke occurrence.

---

## Dataset

* Source: Kaggle Stroke Dataset
* Features include:

  * Age
  * Hypertension
  * Heart disease
  * Smoking status
  * BMI
  * Glucose level
  * Stroke outcome (target variable)

---

## Feature Engineering

A proxy variable for mental stress was created:

df['mental_stress'] = (df['smoking_status'] == 'smokes') * 1

This assumes active smokers may experience higher levels of psychological stress.

---

## Exploratory Data Analysis

### Stroke Distribution

![Stroke Distribution](https://github.com/cindycc88x-neko/stroke-mental-health-analysis/blob/main/stroke.jpg?raw=true)

Stroke cases are relatively rare in the dataset, indicating strong class imbalance.

---

### Average Age by Stroke Status

![Age Analysis](https://github.com/cindycc88x-neko/stroke-mental-health-analysis/blob/main/age.jpg?raw=true)

Stroke patients tend to be significantly older than non-stroke individuals.

---

### Stroke Rate by Smoking Status

![Smoking Analysis](https://github.com/cindycc88x-neko/stroke-mental-health-analysis/blob/main/smoking.jpg?raw=true)

Individuals with a smoking history show a higher risk of stroke, suggesting lifestyle-related influence.

---

### Stroke Rate by Mental Stress Proxy

![Mental Stress Analysis](https://github.com/cindycc88x-neko/stroke-mental-health-analysis/blob/main/stress.jpg?raw=true)

The stress proxy group demonstrates a slightly higher stroke rate, indicating a potential relationship between psychological stress and stroke risk.

---

## Modeling

### Model Used

* Logistic Regression

### Handling Class Imbalance

class_weight='balanced' was used to improve model performance on minority (stroke) cases.

---

## Model Performance

| Metric             | Value |
| ------------------ | ----- |
| Accuracy           | ~0.73 |
| Recall (Stroke)    | ~0.61 |
| Precision (Stroke) | ~0.10 |

---

## Key Insights

* Age is a strong predictor of stroke
* Mental stress proxy (based on smoking) shows a potential association
* Class imbalance significantly affects prediction performance
* The model prioritises recall over precision, which aligns with medical risk detection needs

---

## Tools Used

* Python
* Pandas
* Matplotlib
* Scikit-learn

---

## Author

Shuran Cui
MSc Health Data Science (Incoming), University of Manchester
