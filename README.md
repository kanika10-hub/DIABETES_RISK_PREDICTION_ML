#  Diabetes Risk Prediction using Logistic Regression

A complete Machine Learning project demonstrating the end-to-end workflow of predicting diabetes risk using Logistic Regression.

This project covers:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Preprocessing
- Logistic Regression
- Model Evaluation
- Manual Probability Calculation
- Risk Prediction for New Patients
- Visualization of Evaluation Metrics

---

# Dataset

The dataset contains the following features:

| Feature | Description |
|----------|-------------|
| glucose_level | Plasma glucose level |
| bmi | Body Mass Index |
| blood_pressure | Diastolic Blood Pressure |
| age | Patient Age |
| insulin_level | Serum Insulin |
| skin_thickness | Skin Fold Thickness |
| family_history | Diabetes in Family (Yes/No) |
| physical_activity | Low / Moderate / High |
| diabetic | Target Variable |

The dataset intentionally contains:

- Missing values
- Duplicate rows
- Outliers
- Invalid values
- Mixed categorical labels

to demonstrate a complete data cleaning workflow.

---

# Workflow

```
Raw Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Encoding
      │
      ▼
Feature Scaling
      │
      ▼
Train-Test Split
      │
      ▼
Logistic Regression
      │
      ▼
Evaluation
      │
      ▼
Prediction
```

---

# Exploratory Data Analysis

The project includes:

- Missing Value Analysis
- Correlation Heatmap
- Histograms
- Pairplot
- Boxplots
- Outlier Detection

---

# Data Preprocessing

Performed:

- Removed duplicates
- Handled missing values
- Fixed categorical inconsistencies
- Label Encoding
- Standard Scaling

---

# Model

Algorithm:

- Logistic Regression

Libraries:

- Scikit-learn
- NumPy
- Pandas
- Matplotlib

---

# Model Evaluation

Metrics:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Visualizations:

- Confusion Matrix
- ROC Curve
- Feature Importance
- Probability Distribution

---

# Manual Logistic Regression Calculation

One section of the notebook manually computes:

z = β₀ + β₁x₁ + β₂x₂ + ...

followed by

P = 1 / (1 + e⁻ᶻ)

to explain how Logistic Regression generates probabilities.

---

# Predicting New Patients

A reusable prediction function accepts:

- Glucose Level
- BMI
- Blood Pressure
- Age
- Insulin
- Skin Thickness
- Family History
- Physical Activity

and predicts:

- Diabetes Risk
- Probability
- Final Decision

---

# Results

Example:

Accuracy : 95%

ROC-AUC : 0.97

---

# Project Structure

```
data/
images/
model/
notebook/
src/
README.md
requirements.txt
```

---

# Installation

```bash
git clone https://github.com/yourusername/diabetes-risk-prediction-ml.git

cd diabetes-risk-prediction-ml

pip install -r requirements.txt
```

---

# Run

Open

```
notebook/diabetes_risk_prediction.ipynb
```

or

```bash
python src/train.py
```

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Logistic Regression

---

# Author

Kanika Rathore

LinkedIn:
https://linkedin.com/in/kanika-rathore-682b7a365

GitHub:
https://github.com/kanika10-hub
