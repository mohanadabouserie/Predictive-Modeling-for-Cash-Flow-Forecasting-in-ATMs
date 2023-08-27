# Predictive-Modeling-for-Cash-Flow-Forecasting-in-ATMs

This project involves the implementation of a predictive model for forecasting ATM cash flow using historical transaction data. The project covers data preprocessing, exploratory data analysis, feature engineering, and the construction of predictive models.

## Table of Contents
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Engineering](#feature-engineering)
- [Model Construction](#model-construction)
- [Conclusion](#conclusion)
- [Summary](#Summary)

## Introduction

The primary goal of this project is to develop a predictive model capable of forecasting the cash flow of ATMs using historical transaction data. By understanding the trends and patterns in ATM transactions, the model aims to provide accurate predictions for future cash flow, enabling proactive management of ATM networks.

## Data Preprocessing

The initial phase of the project involves data preprocessing to ensure that the data is clean and ready for analysis. This includes:
- Loading the transaction data into a Pandas DataFrame.
- Converting 'Transaction Date' to datetime format.
- Handling NULL values and missing data.
- Encoding categorical variables using LabelEncoder and get_dummies.
- Normalizing relevant columns using MinMaxScaler.

## Exploratory Data Analysis

Exploratory Data Analysis (EDA) is crucial for gaining insights from the data. Key EDA steps include:
- Grouping data by 'ATM Name' and 'Transaction Date' to analyze cash flow trends.
- Plotting the number of XYZ Card withdrawals and Other Card withdrawals over time.
- Creating line plots for withdrawn amounts over time.
- Visualizing cash flow patterns for all ATMs using bar plots.

## Feature Engineering

Feature engineering plays a vital role in enhancing the predictive power of models. In this project, we:
- Create lag columns to capture historical transaction behavior.
- Calculate Simple Moving Averages (SMA) and Exponential Moving Averages (EMA) for selected features.
- Analyze correlations between features and the 'Total amount Withdrawn' target variable.
- Visualize correlations through heatmap-style plots and bar plots.

## Model Construction

For predictive modeling, we utilize various machine learning techniques, including:
- XGBoost regression model.
- BayesianRidge, RidgeCV, Lasso, RANSACRegressor, Ridge, and LinearRegression models.
- LazyRegressor to evaluate multiple regression models.

## Conclusion
In conclusion, after a thorough exploration of various predictive models and a comprehensive evaluation of their performance, the chosen model for forecasting ATM cash flow is Linear Regression with K-Fold cross-validation. This decision is grounded in several key observations that validate the reliability of this model for addressing the specific problem at hand.

Firstly, the Linear Regression model demonstrated the highest Test score (86%) among the considered models. This achievement suggests that the model's predictive capability extends beyond the training data and performs consistently well on previously unseen data, which is a crucial aspect in ensuring the model's generalization to real-world scenarios.

Furthermore, the model's performance exhibited the least disparity between Test and Train Scores (91.5% - 86% = 5.5%). This careful balancing act is instrumental in avoiding the overfitting of the model. By achieving a close alignment between training and test performance, the Linear Regression model effectively captures the underlying patterns in the data without succumbing to the pitfalls of memorization or lack of adaptability to new information.

In addition, the Linear Regression model showcased the least Mean Absolute Error (MAE) when compared to alternative models (69368.45). MAE is a critical metric as it quantifies the average absolute difference between the predicted and actual values. The lower MAE indicates that the model's predictions are consistently closer to the actual values, implying a higher level of accuracy in its forecasts.

Taking into account the combined strengths of achieving the highest Test score, mitigating overfitting concerns, and yielding the least MAE, the Linear Regression model with K-fold cross-validation emerges as a reliable and robust solution for the ATM cash flow forecasting problem. Its consistent performance across different data subsets and its ability to capture meaningful patterns in the data position it as a valuable tool for decision-making and planning in this context.

It is worth noting that while the Linear Regression model has demonstrated its reliability within the current context, continued monitoring and periodic reevaluation of its performance against changing data patterns is essential to ensure its continued accuracy and relevance.

## Summary
The project showcases the end-to-end implementation of a predictive model for ATM cash flow forecasting. By leveraging data preprocessing, exploratory data analysis, feature engineering, and predictive modeling techniques, the model provides insights into the dynamic patterns and trends influencing ATM transactions.

The developed model's predictions can assist ATM network managers in making informed decisions, optimizing resource allocation, and responding proactively to changes in transaction behavior. The insights obtained from this project contribute to efficient ATM network management and cash flow prediction.

For more details, refer to the code provided in this repository.
