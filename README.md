# Predictive Modeling of House Prices

This repository contains my data science approach to the Kaggle House Prices Competition. This project focuses on predicting residential home prices using a combination of statistical analysis and machine learning.

## 📌 Project Overview
The goal of this project is to build a robust regression model to predict the `SalePrice` of homes. This involves handling a high-dimensional dataset (79 features) and performing feature engineering to extract more meaningful insights from time-based data.

## 📊 Performance Summary
The models were trained on the original price scale to maintain direct interpretability of the error in dollars.

| Model | R2 Score |
| :--- | :--- |
| **XGBoost Regression** | **0.8615** |
| **Linear Regression** | 0.7467 |

## 🛠️ Feature Engineering & Methodology

### 1. Temporal Feature: "Year Used"
One of the most impactful features I engineered was the **Year Used** variable. Instead of simply looking at the year a house was built, this variable calculates the effective age of the property at the time of sale:
*   **Formula:** `Year Sold - Year Built`
*   **Impact:** This allowed the model to better capture the depreciation of property value over time, providing a more linear relationship than raw dates.

### 2. Modeling Strategy
*   **XGBoost:** I utilized an extreme gradient boosting regressor to capture non-linear relationships and interactions between features (like quality vs. age).
*   **Linear Regression:** Used as a baseline model to evaluate the fundamental linear correlations within the dataset.

## 📂 Data Source
The dataset for this project is provided by **Kaggle** as part of the "House Prices - Advanced Regression Techniques" competition. 

*   **Source:** [Kaggle Ames Housing Dataset](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)
*   **Description:** 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa.

