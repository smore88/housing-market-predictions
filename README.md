# House Prices Prediction Project

## Overview

This project is focused on developing predictive models to estimate the sale prices of houses based on a diverse set of features. Our goal is to employ advanced regression techniques to create a robust model that accurately predicts house prices based on characteristics like the area, number of rooms, garage type, and many others.

## Dataset

The dataset includes a comprehensive set of features about the physical attributes of residential homes. Key features include:

- `OverallQual`: Overall material and finish quality
- `GrLivArea`: Above grade (ground) living area square feet
- `GarageCars`: Size of garage in car capacity
- `TotalBsmtSF`: Total square feet of basement area
- `FullBath`: Full bathrooms above grade
- `YearBuilt`: Original construction date

The target variable is `SalePrice`, which we aim to predict.

## File Descriptions

- `train.csv` - the training set containing details of houses and their sale prices.
- `test.csv` - the test set where predictions are to be made, without the sale prices.
- `data_description.txt` - full description of each column.

## Model Development

We use various regression models, including but not limited to:
- Linear Regression
- Ridge Regression
- Gradient Boosting Regressor

Each model is evaluated based on the root-mean-squared error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales prices. Such a transformation ensures that errors in predicting expensive houses and cheap houses will affect the result equally.
