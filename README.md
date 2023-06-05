# Housing Price Prediction using Multiple Linear Regression

This project aims to predict housing prices using a multiple linear regression model. The dataset used for this project contains various features related to housing characteristics, such as the year built, living area, garage capacity, and total square footage.

## Overview

The dataset for this project was obtained from the The Ames Housing dataset, compiled by Dean De Cock for data science project use on Kaggle.

In this project, we performed the following steps:

- Data exploration: We analyzed the dataset to understand the available features and their relationships with the target variable (sale price).
- Data preprocessing: We handled missing values through median imputation and performed feature engineering to prepare the data for modeling.
- Model selection and evaluation: We trained the model based upon selected features from the train.csv file and assessed the performance of the multiple linear regression using R-squared score and mean squared error.
- Prediction: We made predictions on the test dataset using the selected model.

## Installation

To run this project, you need to have Python and the following libraries installed:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## Results

The analysis and modeling process led to the following key results:

Upon completion of model tuning, the random forest and bagging models resulted in R2 scores of 0.97 and 0.983 respectively, indicating that our models accounted for ~97% of variance in the data, while the remaining ~3% may be attributed to inherent randomness or factors not included in the model.

The kaggle submission is evaluated upon RMSE and our random forest model received a score of 0.177.

## Next Steps

While we acheived a high R2 score and a submission score of 0.177, there are steps we can take to improve our models:

*   The 'SalePrice' distribution is right skewed with multiple outliars. Our model performance would benefit from normalizing the sale price distribution and performing imputation or removal as necessary for the outliers.

*   There are outliars in many of our selected features: ('OverallQual', 2), ('YearBuilt', 6), ('GarageArea', 7), ('TotalRms', 10), ('TotalSF', 11), ('GrLivArea', 16). To ensure that these values are not negatively influencing our predictions, testing should be performed after treating the missing values.

*   The adaptive boosting model (ADAboost) used for gradient boosting did not result in a strong R2 score, even following model tuning. ADA boost is also sensitive to unneded features; I would like to include XGboost models in testing as they are regularized and less sensitive to overfitting in linear regression models.
