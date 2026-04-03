# Mental Health and Stroke Risk Analysis

## Background

Stroke is one of the leading causes of death and disability worldwide. While traditional risk factors such as age, hypertension, and heart disease are well studied, the role of mental health in stroke risk remains less explored. Understanding the potential relationship between psychological stress and stroke risk could improve early detection and prevention strategies.

---

## Objective

This project aims to investigate whether mental health-related factors are associated with stroke risk and to evaluate whether incorporating such factors can improve predictive performance.

---

## Methods

* Dataset: Stroke Prediction Dataset (public healthcare dataset)
* Data Processing: Cleaned and explored variables including age, BMI, hypertension, heart disease, and smoking status
* Feature Engineering:

  * Created a proxy variable `mental_stress` based on smoking status to represent psychological stress
* Analysis:

  * Exploratory Data Analysis (EDA)
  * Group comparisons (age, smoking, mental stress vs stroke)
* Modeling:

  * Logistic Regression
  * Addressed class imbalance using `class_weight='balanced'`

---

## Results

* Stroke cases are relatively rare (~5%), indicating strong class imbalance
* Age is a significant risk factor, with stroke patients being substantially older
* Individuals with higher mental stress proxy show a slightly increased stroke rate
* Initial models failed to detect stroke cases due to imbalance
* After adjustment:

  * Recall for stroke cases improved significantly (≈0.71)
  * Demonstrated ability to identify high-risk individuals

---

## Discussion

The results suggest that mental health-related factors may contribute to stroke risk, although the effect is modest.

A key challenge identified is class imbalance, which affects model performance and highlights the difficulty of predicting rare medical events. The trade-off between recall and precision reflects real-world clinical decision-making, where identifying at-risk patients is often prioritised over minimizing false positives.

---

## Limitations

* Mental health variables are approximated using proxy indicators (e.g., smoking)
* Dataset lacks direct measures of depression, anxiety, or stress
* Model performance is limited by data imbalance and feature availability

---

## Future Work

Future research could:

* Incorporate richer mental health data (e.g., clinical psychological indicators)
* Apply advanced models (e.g., Random Forest, XGBoost)
* Explore techniques for handling imbalanced data (e.g., SMOTE)

---

## Impact

This project demonstrates how data-driven approaches can support healthcare decision-making. It highlights the importance of integrating mental health into stroke risk assessment and provides a foundation for further research in health data science.

---

## Tools & Technologies

* Python (Pandas, NumPy)
* Matplotlib
* Scikit-learn

---

## Author

Shuran Cui
MSc Health Data Science (Incoming), University of Manchester
