# Future Sales Prediction

This project is a solution to the "Predict Future Sales" competition hosted by Coursera in collaboration with Kaggle. The objective of the competition is to predict daily sales for every product and store for the upcoming month using a challenging time-series dataset provided by 1C Company, one of Russia’s largest software firms. This project served as the final project for the Coursera course "How to Win a Data Science Competition."

## Project Overview

The dataset consists of daily sales data across multiple stores and products, presenting an ideal setting for exploring time-series forecasting, feature engineering, and machine learning model tuning. This repository contains a detailed solution where we predict the future sales by employing various data science techniques and model optimization methods.

## Objective

To predict total sales for every product and store in the next month using a dataset containing historical daily sales data.

### Evaluation Metric

The evaluation metric for this competition is **Root Mean Squared Error (RMSE)**, which measures the standard deviation of residuals between the predicted and actual sales values. Lower RMSE scores indicate a better fit of the model to the data.

## Approach

### 1. Data Preprocessing

- **Missing Data Handling**: Identified and handled missing values where applicable.
- **Data Transformation**: Adjusted features to better represent time-series patterns and improve the model’s interpretability.
- **Aggregation**: Aggregated data at the monthly level, as the prediction was required at this granularity.

### 2. Feature Engineering

- **Lag Features**: Introduced lagging techniques to create historical features that capture previous sales trends for each store-product combination. This included features such as sales in previous months, average sales, and sales trends.
- **Date-related Features**: Extracted month and year features to help the model understand seasonality.
- **Other Features**: Created additional derived features based on domain knowledge, such as rolling mean sales, previous month’s sales, and cumulative sales.

### 3. Modeling

- **Model Choice**: The LightGBM (LGBM) model was used as it is well-suited for time-series forecasting and handling large datasets efficiently.
- **Hyperparameter Tuning**: Optimized hyperparameters using grid search and cross-validation to improve the model's performance and reduce overfitting.
- **Cross-validation**: Implemented time-series cross-validation to ensure that the model performs well on unseen future data and generalizes effectively.

### 4. Evaluation

- **Public Score**: The model achieved a public leaderboard score of **0.91380** on RMSE, showcasing its effectiveness on the given dataset.

## Key Learnings

This project provided valuable experience with:

- **Lagging Techniques**: The addition of lagging features to improve prediction accuracy.
- **Hyperparameter Tuning**: Fine-tuning model parameters for optimal performance.
- **LightGBM**: Leveraging LightGBM’s gradient boosting capabilities to handle large datasets with ease and speed, making it ideal for competitive time-series forecasting tasks.

## Results

With careful feature engineering, hyperparameter tuning, and model selection, the project resulted in an RMSE score of **0.91380** on the public leaderboard, validating the effectiveness of the LightGBM model and feature engineering techniques for this time-series forecasting challenge.
