# Feature Scaling

## Project Overview

This project is a Python script that demonstrates how to load a dataset, split it into training and test sets, and apply feature scaling using the `StandardScaler` from the `sklearn.preprocessing` module. The dataset used in this project is the Wine Quality Red dataset, which is included in the project files as `winequality-red.csv`.

## How It Works

The script begins by importing the necessary libraries: `pandas`, `sklearn.model_selection`, and `sklearn.preprocessing`.

The Wine Quality Red dataset is loaded into a pandas DataFrame using the `pd.read_csv()` function. The features (independent variables) and the target (dependent variable) are then separated. The features are all columns except the last one, and the target is the last column.

The dataset is then split into a training set and a test set using the `train_test_split()` function from `sklearn.model_selection`. The split is done in an 80-20 ratio, meaning 80% of the data goes to the training set and 20% goes to the test set.

After splitting the data, feature scaling is applied to both the training and test sets. Feature scaling is a preprocessing step that is often necessary in machine learning to make sure that all features have the same scale. This is important because many machine learning algorithms are sensitive to the scale of the features.

## StandardScaler

The `StandardScaler` from `sklearn.preprocessing` is used for feature scaling. It standardizes features by removing the mean and scaling to unit variance. The standard score of a sample `x` is calculated as:

`z = (x - u) / s`

where `u` is the mean of the training samples, and `s` is the standard deviation of the training samples.

The `StandardScaler` is fitted to the training data using the `fit()` method, which computes the mean and standard deviation to be used for later scaling. Then, the `transform()` method is used to perform the standardization by centering and scaling.

The `fit_transform()` method is a convenience method that fits the data and then transforms it. However, it's important to note that the scaler should be fitted on the training data and not the test data. The same scaling (i.e., the same mean and standard deviation) should be applied to both the training data and the test data for correct results.

## Running the Script

To run the script, simply execute the `exercise.py` file in a Python environment that has the necessary libraries installed. The script will print the scaled training and test sets to the console.