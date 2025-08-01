# income-prediction

I built and tested ML models to predict whether someone makes more than $50K a year based on U.S. census data. This was a chance to practice data cleaning, feature engineering, and compare model performance.

## Overview

This project uses the UCI Adult Income dataset to predict income level from features like age, education, occupation, and marital status. The goal was to figure out which models work best and what features are most important for this kind of task.

## Goals

- Predict if someone earns over $50K using ML
- Explore data preprocessing and feature selection
- Handle class imbalance
- Compare models based on precision, recall, and F1-score

## Steps I Took

### 1. Data Cleaning
- Dropped rows with missing values
- Removed duplicate features like `education` and `education-num` to avoid redundancy
- Checked for class imbalance in the labels

### 2. Feature Engineering
- Applied one-hot encoding to all categorical columns
- Normalized numerical columns
- Looked at feature correlations to remove noise

### 3. Model Training
- Trained Logistic Regression, Decision Tree, and Random Forest
- Tried out SMOTE and class weighting to handle class imbalance
- Compared accuracy and F1-score for each

### 4. Model Selection
- Random Forest had the best F1-score overall
- Most useful features: `education-num`, `capital-gain`, and `marital-status`

## Key Results

- F1-score: ~0.78 with Random Forest
- Accuracy alone was misleading due to class imbalance
- Class weighting helped improve recall for the minority class

## Visuals

- Correlation heatmap for numerical features
- Class balance before and after SMOTE
- Confusion matrix for final model

## Try It Out

You can run the project using Jupyter:

```bash
git clone https://github.com/YOUR_USERNAME/income-prediction.git
cd income-prediction
pip install -r requirements.txt
jupyter notebook income_prediction.ipynb

