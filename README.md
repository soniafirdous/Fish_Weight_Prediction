# Fish Weight Prediction 🐟

Predicting the weight of fish using machine learning models based on physical measurements like length, width, and height. This project demonstrates how data science can be applied to aquaculture analytics and real-world predictions.

## 📂 Project Overview

Accurate prediction of fish weight is important in aquaculture for monitoring growth, optimizing feed, and managing resources. This project explores Smelt fish data and builds machine learning models to estimate weight from measurements.

## 🔹 Features

Analysis of fish measurements: Length1, Length2, Length3, Height, Width

Weight prediction using machine learning models

Data cleaning, preprocessing, and exploratory data analysis

Model evaluation for accuracy and performance

## 🛠️ Technologies Used

Python

Pandas & NumPy

Scikit-learn (Regression Models)

Matplotlib & Seaborn (Visualization)

## 📊 Workflow

Data Loading & Cleaning: Handle missing values, remove inconsistencies.

Exploratory Data Analysis: Understand relationships between measurements and weight.

Feature Selection & Engineering: Use relevant measurements for prediction(avg_lenghth & PCA_length)

Model Building: Train machine learning models to predict fish weight.

Evaluation: Compare predicted vs actual weight, calculate model loss and R2 score.

## 📊 Model Performance Analysis

| Model           | MAE        | RMSE       | R²        |
|-----------------|------------|------------|-----------|
| Polynomial      | 30.41      | 43.98      | 0.9864    |
| Random Forest   | 50.89      | 79.11      | 0.9560    |
| XGBoost         | 49.04      | 85.13      | 0.9491    |
| Linear          | 67.57      | 89.48      | 0.9437    |
| Decision Tree   | 68.40      | 111.45     | 0.9127    |
| SVR             | 302.05     | 393.49     | -0.0886   |


## 🥇 Best Model: Polynomial Regression

Polynomial Regression outperformed all other models by effectively capturing the non-linear relationship between fish dimensions and weight, achieving the highest R² and lowest error metrics.

Lowest MAE: 30.40

Lowest RMSE: 43.98

Highest R²: 0.986

✅ Captures the non-linear relationship between fish size and weight extremely well.

⚠️Over fitting check:

Training MSE: 1351.49
Testing MSE: 1933.98

Overfitting was assessed using train–test MSE comparison, indicating mild overfitting due to limited sample size and polynomial complexity.

🥈 Random Forest

R²: 0.956

Strong generalization

Handles non-linearity & interactions naturally

✅ Very robust
❌ Slightly less accurate than polynomial regression here

🥉 XGBoost

R²: 0.949

Competitive performance

Slightly higher RMSE than RF

✅ Powerful ensemble method
⚠️ Needs tuning for best performance

🔹 Linear Regression

R²: 0.944

Reasonable baseline

✅ Simple and interpretable
❌ Cannot fully capture non-linearity

🔹 Decision Tree

R²: 0.913

Higher RMSE

⚠️ Overfits small datasets
❌ Less stable than ensemble models

❌ Worst Model: SVR

Negative R² (-0.089)

Very high MAE & RMSE

🚨 Performs worse than predicting the mean
Likely reasons:

Poor kernel choice

Inadequate hyperparameters

Sensitive to scaling and small dataset size

## 🙋‍♀️Author

Sonia Firdous

