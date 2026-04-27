# Shinkansen Travel Experience Prediction

## Overview
This project predicts passenger satisfaction for the Shinkansen Bullet Train using machine learning.

The model was developed as part of a hackathon and achieved Rank 1 on the leaderboard with an accuracy of 0.9524465.

---

## Problem Statement
The objective is to classify whether a passenger is satisfied (1) or not satisfied (0) based on:

- Travel data (distance, delays, class)
- Service feedback (comfort, cleanliness, catering, etc.)

---

## Dataset
The dataset consists of two components:

- Travel Data: Passenger and journey-related attributes
- Survey Data: Post-travel service ratings

Both datasets were merged using a common identifier (ID).

---

## Approach

### Data Preprocessing
- Merged travel and survey datasets
- Handled missing values using median (numerical) and default categories (categorical)
- Ensured consistency between training and testing data

### Feature Engineering
The following features were created to improve model performance:

- Total_Delay: Combined arrival and departure delay
- Service_Mean: Average service rating
- Service_Std: Variation in service ratings
- High_Service_Count: Count of high ratings
- Low_Service_Count: Count of low ratings
- Delay_Impact: Interaction between delay and service quality
- Experience_Score: Combined metric of service and delay

### Model
A LightGBM classifier was used due to its effectiveness on structured data.

Key parameters:
- n_estimators = 4000
- learning_rate = 0.01
- num_leaves = 128
- subsample = 0.9
- colsample_bytree = 0.9

Categorical variables were encoded using one-hot encoding to avoid ordinal bias.

---

## Results
- Accuracy: 0.9524465
- Rank: 1

---

## Key Insights
- Service quality is the strongest predictor of passenger satisfaction
- Consistency across services is more important than isolated high ratings
- Delay impacts satisfaction, but high service quality can mitigate its effect

---

## Tech Stack
- Python
- Pandas
- NumPy
- LightGBM
- Scikit-learn

---

## Project Structure

shinkansen-satisfaction-prediction/
│
├── notebook/
│   └── final_solution.ipynb
├── submission/
│   └── submission_V8_FINAL.csv
├── README.md
├── requirements.txt

---

## How to Run

Install dependencies:
pip install -r requirements.txt

Run the notebook:
notebook/final_solution.ipynb

---

## Author
Prabhjot Singh
