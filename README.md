# Housing Price Prediction using Multiple Linear Regression

This project aims to predict housing prices using a multiple linear regression model. The dataset used for this project contains various features related to housing characteristics, such as the year built, living area, garage capacity, and total square footage.

## Overview

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

The multiple linear regression model achieved an R-squared score of 0.76 on the training data.
Scatter plots were created to visualize the relationships between selected features and the sale price.

Based upon the predictions uploaded to kaggle, we achieved a R-squared score of 0.72 on the test data.

## Next Steps

The R-squared score of 0.72 indicates that our model accounts for 72% of the variance in the target prediction, however there are a few highly correlated variables which may cause overfitting.

To improve the accuracy of our prediction, I will continue by using the standard scaler feature in scikit and perform testing on non-linear models such as decision trees and random forest.
