# Logistic Regression Classification

## Overview

Logistic Regression is a Machine Learning classification algorithm that is used to predict the probability of a categorical dependent variable. In logistic regression, the dependent variable is a binary variable that contains data coded as 1 (yes, success, etc.) or 0 (no, failure, etc.). In other words, the logistic regression model predicts P(Y=1) as a function of X.

## Calculation

Logistic Regression uses the concept of odds ratios. The odds ratio can be defined as the ratio of the odds of an event happening to its not happening. The odds ratio for a variable in logistic regression represents how the odds change with a 1 unit increase in that variable holding all other variables constant.

The logistic regression equation has a similar concept to the linear regression. The difference is that in linear regression we use linearity of unknown parameters, but logistic regression is based on the natural logarithm function. The standard logistic function is given as:

```
P(X) = e^(b0 + b1*X) / (1 + e^(b0 + b1*X))
```

Where:
- P(X) is the probability of the event occurring.
- e is the base of natural logarithms.
- b0 is the y-intercept.
- b1 is the slope.
- X is the independent variable (predictor).

## When to Use Logistic Regression

Logistic regression is used when the dependent variable is binary(0/1, True/False, Yes/No) in nature. Here are a few situations where logistic regression is applicable:

1. Weather predictions (Rain: Yes/No)
2. Classification problems (Spam: Yes/No)
3. Medicine (Disease: Yes/No)
4. Marketing applications (Will the customer buy this product: Yes/No)

## Project Overview

In this project, we use Logistic Regression to predict whether a user will purchase a product or not based on their age and estimated salary. The dataset `Social_Network_Ads.csv` contains information about users, and the model is trained and tested using this data. The model's performance is evaluated using a confusion matrix and accuracy score.