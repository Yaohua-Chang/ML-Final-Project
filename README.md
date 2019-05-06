# House Prices: Advanced Regression Techniques

## Abstract
Predict sales prices with advanced regression techniques and practice feature engineering.

## Introduction
This is our team's final project for Applied Machine Learning course. This team is consisted of Wenyu Fan, Tamer Ibranhim and Yaohua Chang. 

## Background
This dataset was constructed by Dean De Cock for use in Data Science education. It is viewed as a modern alternative to the Boston Housing dataset.

This dataset iseasy to understand so that we can put most time on studying and applying machine learning techniques rather than trying to understand it.

In addition, The community concerning this dataset is large so that we can study lots of brilliant ideas from there.

## Data
Dataset from Kaggele:  
https://www.kaggle.com/c/house-prices-advanced-regression-techniques

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this project challenges us to predict the final price of each home.

## Method
### Data Preprocessing
* Dealing with missing values
    * Filling LotFrontage NaN values using a linear regression model. 

* Dealing with zeros  
    Adding dummy variables for features with a lot of zeros to improve model fits.

* Encoding categorical variables

* Creating new features
    * Creation of features for different basement finish types.

* transform target variable into normal distribution

* Remove outliers

### Exploratory Data Analysis
* Distribution of SalePrice for all the features

* Correlation between the features and SalePrice (or each other)

### Feature Selection
As we can see there are many features in this dataset.Random forest can be used to do feature selection to remove least important features. 

### Fit and Optimise Models
To avoid repeating code I create a function to perform the fitting process for each model type I try. I use k-fold cross-validation to reduce the chances of overfitting the training data - specifically 5-fold cross-validation repeated 5 times. 

The parameters of each model are optimised using a grid search, and the function returns the best model found and some stats on the model performance.

The models we tried are:
* Linear Regression:
    * sklearn.linear_model.Ridge
    * sklearn.linear_model.Lasso
    * sklearn.linear_model.ElasticNet

* Support Vector Machines:
    * sklearn.svm.LinearSVR
    * sklearn.svm.SVR

* Nearest Neighbours:
    * sklearn.neighbors.KNearestNeighborsRegressor

* Tree Based:
    * sklearn.ensemble.RandomForestRegressor
    * sklearn.ensemble.GradientBoostingRegressor


## Evaluation

## Conclusion