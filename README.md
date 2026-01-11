# 🛍️📊 HR Employee Attrition Prediction – Random Forest
![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)  
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-1.2-orange?logo=scikit-learn)  
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)  
![License](https://img.shields.io/badge/License-MIT-green)  

End-to-end ML project | **Random Forest Classification** to predict employee attrition (stay vs quit)  
Built by Abdelrahman Alabadla • Jan 2026  
Email: abdelrahmanalabadla@gmail.com  

---

## Overview
Employee attrition is costly for companies. This project predicts whether an employee is likely to **stay or leave**, helping HR take proactive measures.  

- **Problem Type:** Binary Classification  
- **Target Variable:** `Attrition` (0 = Stay, 1 = Quit)  
- **Algorithm:** Random Forest Classifier  

---

## Dataset
- **Records:** 1,470 employees  
- **Features:** 35 (demographics, job info, performance metrics)  
- **Sample Features:** Age, Gender, Department, Job Role, Job Satisfaction, Work-Life Balance, Years at Company  

---

## Data Preprocessing
- Handle missing values (none in this dataset)  
- Convert categorical variables to numeric:  
  - Binary mapping (e.g., Gender, OverTime, Attrition)  
  - One-hot encoding for multi-class features (e.g., Department, JobRole)  
- Scale numeric features with **StandardScaler**  
- Split data into **train (75%) and test (25%)**  

---

## Modeling
- **Random Forest Classifier** with tuned hyperparameters  
- Addressed **class imbalance** with class weights and threshold adjustment  
- Model trained to predict attrition probability  

**Performance on Test Set:**  
- Accuracy: ~0.81  
- F1-score for attrition class: 0.42  
- Train-Test Gap: 0.06 (no significant overfitting)  

---

## Sample Prediction
You can test the model on any employee using a dictionary of features:  

```python
if sample_pred[0] == 1:
    print("This employee will likely quit.")
else:
    print("This employee will likely stay.")

This employee will likely quit.  
Predicted probability of leaving: 0.70

