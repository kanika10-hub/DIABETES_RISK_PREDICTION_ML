#  Project Walkthrough (Diabetes Risk Prediction using Logistic Regression)

##  Project Overview

This project demonstrates an end-to-end Machine Learning workflow for predicting whether a patient is at risk of diabetes using **Logistic Regression**.

The objective is not only to build a prediction model but also to understand every stage involved in a real-world machine learning pipeline from raw data preprocessing to model interpretation and prediction.

---

# Project Workflow

```
Patient Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Exploratory Data Analysis (EDA)
      │
      ▼
Feature Engineering
      │
      ▼
Feature Scaling
      │
      ▼
Train-Test Split
      │
      ▼
Logistic Regression Model
      │
      ▼
Model Evaluation
      │
      ▼
Model Interpretation
      │
      ▼
Prediction for New Patients
```

---

# Step 1 — Understanding the Problem

### Objective

Develop a machine learning model capable of predicting whether a patient is diabetic based on medical and lifestyle-related attributes.

### Features Used

- Glucose Level
- BMI (Body Mass Index)
- Blood Pressure
- Age
- Insulin Level
- Skin Thickness
- Family History
- Physical Activity

### Target Variable

```
Diabetic

Yes → 1
No  → 0
```

---

# Step 2 — Dataset Preparation

A synthetic healthcare dataset was created to simulate real-world patient records.

Unlike perfectly clean datasets, this one intentionally contains several common data quality issues.

### Introduced Data Issues

- Missing values
- Duplicate records
- Outliers
- Invalid numerical values
- Mixed data types
- Inconsistent categorical labels
- Extra whitespace
- Mixed capitalization

### Why?

Real-world datasets are rarely clean. Practicing on imperfect data helps develop practical preprocessing skills used in industry.

---

# Step 3 — Data Cleaning

Before training any model, the dataset must be cleaned.

The following preprocessing steps were performed:

- Removed duplicate rows
- Identified and handled missing values
- Corrected inconsistent category names
- Converted incorrect data types
- Removed unnecessary whitespace
- Validated numerical ranges
- Detected and handled outliers

### Why?

Machine Learning models assume that input data is consistent and reliable. Poor-quality data often leads to inaccurate predictions.

---

# Step 4 — Exploratory Data Analysis (EDA)

EDA was performed to better understand the dataset before building the model.

### Visualizations Created

- Histograms
- Boxplots
- Correlation Heatmap
- Pair Plot
- Feature Distributions

### Objectives

- Understand feature distributions
- Detect skewed variables
- Identify outliers
- Discover relationships between features
- Analyze class distribution

---

# Step 5 — Feature Engineering

Machine learning algorithms require numerical inputs.

Therefore, categorical features were converted into numerical values.

### Family History

| Original | Encoded |
|----------|---------|
| No | 0 |
| Yes | 1 |

### Physical Activity

| Original | Encoded |
|----------|---------|
| High | 0 |
| Low | 1 |
| Moderate | 2 |

The target variable was also converted into binary values.

---

# Step 6 — Feature Scaling

The features have different ranges.

Example:

| Feature | Approximate Range |
|----------|------------------|
| Glucose | 70–200 |
| BMI | 18–40 |
| Age | 20–80 |
| Insulin | 15–300 |

Without scaling, larger numerical values may dominate the learning process.

Therefore, **StandardScaler** was applied to standardize all numerical features.

---

# Step 7 — Train-Test Split

The cleaned dataset was divided into two parts.

```
Training Set : 80%

Testing Set : 20%
```

### Purpose

Training data is used to learn the model parameters.

Testing data is used to evaluate the model on unseen data.

---

# Step 8 — Logistic Regression

A Logistic Regression classifier was trained using the processed dataset.

Unlike Linear Regression, Logistic Regression predicts the probability that an observation belongs to a particular class.

The model first calculates a linear score:

```
z = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ
```

The score is then converted into a probability using the Sigmoid Function.

```
P = 1 / (1 + e⁻ᶻ)
```

Prediction rule:

```
Probability ≥ 0.5
        ↓
 Diabetic

Probability < 0.5
        ↓
 Non-Diabetic
```

---

# Step 9 — Manual Risk Calculation

To understand how Logistic Regression makes predictions internally, the probability calculation was performed manually for a sample patient.

The following steps were carried out:

- Prepared patient input
- Applied feature scaling
- Extracted model coefficients
- Calculated each feature's contribution
- Computed the linear score (z)
- Applied the Sigmoid function
- Obtained the diabetes probability
- Compared the probability with the classification threshold

Finally, the manually computed result was verified against Scikit-Learn's prediction.

This exercise provides insight into how Logistic Regression works mathematically.

---

# Step 10 — Model Evaluation

The trained model was evaluated using standard classification metrics.

## Accuracy

Percentage of correctly classified patients.

---

## Precision

Among all patients predicted as diabetic,

**How many actually are diabetic?**

---

## Recall (Sensitivity)

Among all actual diabetic patients,

**How many were successfully detected?**

Recall is particularly important in healthcare because missing a diabetic patient (False Negative) can have serious consequences.

---

## F1-Score

A balanced metric combining Precision and Recall.

Useful when both false positives and false negatives are important.

---

## ROC-AUC

Measures how well the classifier distinguishes diabetic patients from non-diabetic patients across different thresholds.

Higher AUC indicates better model performance.

---

# Step 11 — Model Visualization

Several visualizations were created to interpret the model.

## Confusion Matrix

Shows

- True Positives
- True Negatives
- False Positives
- False Negatives

This helps identify the types of mistakes made by the model.

---

## ROC Curve

Illustrates the relationship between

- True Positive Rate
- False Positive Rate

A model with a larger area under the curve performs better.

---

## Feature Importance

Logistic Regression coefficients indicate the contribution of each feature.

- Positive coefficient → increases diabetes risk
- Negative coefficient → decreases diabetes risk

This helps explain which features influence the prediction most.

---

## Probability Distribution

Displays predicted diabetes probabilities for both diabetic and non-diabetic patients.

This visualization shows how confidently the model separates the two classes.

---

# Step 12 — Predicting New Patients

A reusable prediction function was created.

The function performs the following steps:

1. Accepts new patient information
2. Encodes categorical variables
3. Applies feature scaling
4. Generates prediction
5. Computes diabetes probability
6. Returns the final decision

This allows the trained model to be used for predicting new patient cases.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Logistic Regression

---

# Machine Learning Concepts Covered

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Label Encoding
- Standardization
- Train-Test Split
- Logistic Regression
- Sigmoid Function
- Binary Classification
- Probability Estimation
- Confusion Matrix
- ROC Curve
- Feature Importance
- Model Interpretation

---

# Conclusion

This project demonstrates a complete supervised machine learning workflow for binary classification using Logistic Regression.

Beyond building a predictive model, the project focuses on understanding the reasoning behind each preprocessing step, the mathematical foundation of Logistic Regression, and the interpretation of evaluation metrics and visualizations.
