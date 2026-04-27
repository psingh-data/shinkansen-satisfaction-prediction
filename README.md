# Shinkansen Travel Experience Prediction

Rank 1 solution with an accuracy of 0.9524465

---

## Overview

This project predicts passenger satisfaction for the Shinkansen Bullet Train using machine learning.

The objective is to classify whether a passenger is satisfied (1) or not satisfied (0) based on travel and service-related attributes.

---

## Problem Statement

Passengers were surveyed after their journey and asked about their overall experience.

The goal is to identify key factors influencing satisfaction and build a model that accurately predicts the outcome.

---

## Dataset

The dataset consists of two parts:

- Travel Data: Contains passenger and journey-related features such as travel distance and delays  
- Survey Data: Contains service ratings such as cleanliness, comfort, catering, and more  

Both datasets are merged using a common ID.

---

## Approach

### Data Preprocessing
- Merged travel and survey datasets  
- Handled missing values  
- Cleaned and standardized categorical variables  

---

### Feature Engineering
Key features created include:

- Total Delay (arrival + departure delay)  
- Service Mean and Standard Deviation  
- High and Low Service Count  
- Delay Impact on Experience  
- Combined Experience Score  

---

### Model

A LightGBM classifier was used due to its efficiency on structured data.

Key parameters:
- n_estimators = 4000  
- learning_rate = 0.01  
- num_leaves = 128  
- subsample = 0.9  
- colsample_bytree = 0.9  

Categorical variables were encoded using one-hot encoding.

---

## Results

- Accuracy: 0.9524465  
- Rank: 1  

---

## Key Insights

- Service quality is the most important factor influencing satisfaction  
- Consistency across services matters more than individual high ratings  
- Delay affects satisfaction, but strong service can offset it  

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
