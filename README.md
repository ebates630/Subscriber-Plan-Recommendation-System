# Megline Subscriber Plan Recommendation

## Overview  
I built a machine learning model that analyzes how people use their phones and predicts whether they’re a better fit for Megaline’s Smart or Ultra plan. The work focused on turning real subscriber behavior data into something that could realistically support plan recommendations.

The model was trained using monthly usage data (calls, minutes, text messages, and mobile internet). I tested multiple modeling approaches, tuned the strongest one, and achieved about **83% accuracy on new users**. Throughout the process, the emphasis was on doing this the right way using proper training, validation, and test splits so the results would hold up beyond the training data.

---

## Problem Framing  
Many telecom customers remain on outdated plans that no longer match how they actually use their service. The goal was to build a classification model that could learn from existing customer behavior and recommend whether a user should be on the Smart or Ultra plan.

This is a binary classification task where the model predicts:  
- `0` → Smart plan  
- `1` → Ultra plan  

---

## Dataset  
Each row represents one user’s monthly behavior:  
- `calls` — number of calls  
- `minutes` — total call duration  
- `messages` — number of texts  
- `mb_used` — mobile data usage  
- `is_ultra` — current plan (target)

---

## Approach  
- Reviewed and explored the dataset  
- Split data into training, validation, and test sets (60/20/20)  
- Built and evaluated multiple models: Decision Tree, Logistic Regression, Random Forest  
- Tuned hyperparameters using validation data  
- Selected the strongest model  
- Performed final testing and sanity checks  

---

## Results  
- Best model: Random Forest Classifier  
- Final test accuracy: ~83%  
- Validation and test scores were consistent, indicating good generalization

---

## Tools  
Python · pandas · NumPy · scikit-learn · Jupyter Notebook

---

## Why this matters  
This work shows how subscriber behavior data can be used to support real telecom decisions improving plan fit, reducing reliance on legacy plans, and enabling data-driven recommendations.

