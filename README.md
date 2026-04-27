# Shinkansen-satisfaction-prediction
Rank 1 solution (95.24% accuracy) – ML model for Shinkansen passenger satisfaction

## Overview
This project predicts passenger satisfaction for the Shinkansen Bullet Train using machine learning.

Achieved **Rank 1** with **95.24% accuracy** in a competitive hackathon.

---

## Problem Statement
Predict whether a passenger is satisfied (1) or not satisfied (0) based on:
- Travel details
- Service ratings

---

## Dataset
The dataset consists of:
- Travel Data
- Survey Data

Merged using a common `ID`.

---

## Approach

### 1. Data Preprocessing
- Handled missing values
- Merged datasets correctly
- Encoded categorical variables using one-hot encoding

---

### 2. Feature Engineering
- Total Delay
- Service Mean & Variance
- High/Low Service Counts
- Delay Impact
- Experience Score

---

### 3. Model
Used **LightGBM Classifier** with tuned parameters:
- n_estimators = 4000
- learning_rate = 0.01
- num_leaves = 128

---

### 4. Result
- Accuracy: **0.9524465**
- Rank: **1**

---

## Key Insights
- Service quality is the strongest predictor
- Consistency matters more than isolated good experiences
- Delay impact depends on service quality

---

## Tech Stack
- Python
- Pandas, NumPy
- LightGBM
- Scikit-learn

---

## How to Run

1. Install dependencies:

## pip install -r requirements.txt

2. Run the notebook:
notebook/final_solution.ipynb


---

## Author
Prabhjot Singh
