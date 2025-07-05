# Blood Donation Prediction Project

![Blood Donation Banner](https://www.kaggle.com/datasets/whenamancodes/blood-transfusion-dataset/data) <!-- Add a relevant image if available -->

A machine learning project to predict the likelihood of blood donors returning to donate again.

## 📊 Model Performance

| Algorithm       | Training Accuracy | 
|----------------|------------------|
| Random Forest  | 90.46%           |
| XGBoost        | 90.34%           | 

**Best Model**: Random Forest (80.71% test accuracy)

## 📋 Project Overview

This project develops a predictive model to identify which blood donors are likely to donate again, helping blood banks optimize their donor outreach programs.

## 🛠️ Technical Implementation

### Data Features
- **Original Features**:
  - Recency (months since last donation)
  - Frequency (total number of donations)
  - Monetary (total blood donated in c.c.)
  - Time (months since first donation)
  
- **Engineered Features**:
  - Donation Rate (Frequency/Time)
  - Recency Ratio (Recency/Time)
  - Activity Index
  - Donor Loyalty Score
  - Recent Donor Flag

### Model Architecture
```python
RandomForestClassifier(
    n_estimators=400,
    max_depth=10,
    min_samples_split=10,
    class_weight={0:1, 1:2},
    random_state=42
)
