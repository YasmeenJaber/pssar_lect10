# Lecture 11:
Many real-world challenges can be addressed using Machine Learning techniques. Before building a model, it is important to frame the business or organizational problem as a machine learning task. This involves identifying the target variable, selecting relevant features, defining the unit of prediction, determining the prediction horizon, choosing appropriate evaluation metrics, and considering potential constraints and risks.

In this report, five real-world scenarios are analyzed and translated into machine learning problems. These scenarios include improving university graduation rates, reducing hospital readmissions, personalizing e-commerce homepages, predicting water pipe failures, and understanding student mental health outcomes. For each case, the problem is structured using a machine learning framework to demonstrate how data-driven solutions can support decision-making and improve outcomes.
1. University wants to improve graduation rates
Target Variable

Will the student graduate on time? (Yes / No)

Features
GPA
Attendance rate
Assignment submission rate
Credits completed
Demographic and enrollment information
Unit of Prediction

One student

Prediction Horizon

At the end of the first academic year (or each semester)

Success Metric

F1-score, Recall, or AUC-ROC

Constraints & Risks
Student privacy
Bias against certain groups
Missing at-risk students (false negatives)
/////////////////////////////////////////////
2. Hospital wants to reduce patient readmissions
Target Variable

Will the patient be readmitted within 30 days? (Yes / No)

Features
Age
Diagnosis
Length of stay
Previous admissions
Medications
Lab results
Unit of Prediction

One patient discharge

Prediction Horizon

At discharge time

Success Metric

Recall, Precision, AUC-ROC

Constraints & Risks
Patient safety
Cost of incorrect predictions
Explainability requirements
//////////////////////////////////////////////////////
3. E-commerce company wants to personalize the homepage
Target Variable

Probability that a user clicks or purchases a recommended item

Features
Browsing history
Purchase history
Search queries
Product ratings
Session behavior
Unit of Prediction

One user-session

Prediction Horizon

Real-time when the homepage loads

Success Metric

CTR (Click-Through Rate), Conversion Rate

Constraints & Risks
Cold-start users
Privacy concerns
Recommendation diversity
/////////////////////////////////////////////////
4. City wants to predict water pipe failures in advance
Target Variable

Will a pipe fail within the next 6 months? (Yes / No)

Features
Pipe age
Material type
Diameter
Pressure readings
Maintenance history
Soil conditions
Unit of Prediction

One water pipe

Prediction Horizon

3–6 months before failure

Success Metric

Recall, Precision, F1-score

Constraints & Risks
High repair costs
Public service disruptions
False alarms causing unnecessary maintenance
///////////////////////////////////////////////
5. Research team wants to understand student mental health outcomes
Target Variable

Mental health risk level (Low / Medium / High)

Features
Academic performance
Attendance
Sleep patterns
Survey responses
Social engagement
Stress indicators
Unit of Prediction

One student

Prediction Horizon

At the end of each semester

Success Metric

Accuracy, F1-score

Constraints & Risks
Privacy and ethics
Sensitive data handling
Risk of misclassification affecting support decisions
-------------------------------------------------------
Project Overview

This project uses the UCI Adult Income dataset to predict whether a person's annual income exceeds $50,000 based on demographic and employment-related features.

Dataset
Dataset: Adult Income Dataset
Source: UCI Machine Learning Repository - Adult Dataset
Target Variable: income
1 → income > 50K
0 → income ≤ 50K
Objective

Build a machine learning pipeline to classify individuals into income categories and establish a baseline model for future improvements.

Data Preprocessing
1. Load and Inspect Data
Loaded dataset using Pandas.
Checked data types, shape, and missing values.
2. Define Target Variable
Converted income into a binary target.
Removed fnlwgt because it is a census weight rather than a predictive feature.
3. Train-Test Split
Split data into 80% training and 20% testing.
Used stratified sampling to preserve class distribution.
4. Handle Missing Values
Numerical features: Median imputation.
Categorical features: Most frequent value imputation.
5. Encode Categorical Variables
Applied one-hot encoding using pd.get_dummies().
Aligned train and test datasets to handle unseen categories.
6. Feature Scaling
Applied StandardScaler to numerical features.
Fitted scaler only on training data to avoid data leakage.
7. Baseline Model
Used DummyClassifier(strategy="most_frequent").
Baseline accuracy ≈ 76%.
Features Used
Age
Workclass
Education
Education Number
Marital Status
Occupation
Relationship
Race
Sex
Capital Gain
Capital Loss
Hours per Week
Native Country
Evaluation Metric
Accuracy
Future models may also be evaluated using Precision, Recall, F1-score, and ROC-AUC.
Technologies
Python
Pandas
NumPy
Scikit-learn
Jupyter Notebook / VS Code
Results

The baseline model achieved approximately 76% accuracy, providing a benchmark for more advanced classification models such as Logistic Regression, Decision Trees, and Random Forests.