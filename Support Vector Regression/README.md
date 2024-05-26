# Support Vector Regression (SVR)

## Overview

This exercise uses Support Vector Regression (SVR) to predict salaries based on position levels. The dataset used is `Position_Salaries.csv`.

### Code Overview

The code first imports necessary libraries and the dataset. It then applies feature scaling to the independent and dependent variables (X and y respectively) using `StandardScaler` from `sklearn.preprocessing`.

The SVR model is trained on the whole dataset (since it's small) using the Radial basis function (RBF) kernel. The model's prediction is then inverse transformed back to the original scale for interpretation.

Finally, the results are visualized using a scatter plot and line plot.

### StandardScaler

`StandardScaler` is a preprocessing utility in the `sklearn.preprocessing` package. It standardizes features by removing the mean and scaling to unit variance. This is often a necessary step as many machine learning algorithms perform better or converge faster when features are on a relatively similar scale and close to a normal distribution.

The `fit_transform` method is used to calculate the mean and standard deviation on the training set and then the scaling (subtracting the mean and scaling by inverse of standard deviation) is applied. The `inverse_transform` method is used to scale the data back to the original representation.

The equation used by `StandardScaler` is:

z = (x - u) / s

Where:
- x is the feature value
- u is the mean of the feature values in the training set
- s is the standard deviation of the feature values in the training set
- z is the standardized value

### SVR and the Kernel Parameter

Support Vector Regression (SVR) is a type of Support Vector Machine (SVM) that supports linear and non-linear regression. The implementation of SVR in this project is from the `sklearn.svm` package.

The `kernel` parameter specifies the kernel type to be used in the algorithm. It must be one of `linear`, `poly`, `rbf`, `sigmoid`, `precomputed` or a callable. If none is given, `rbf` will be used, which is also the case in this project.

The Radial basis function (RBF) kernel, or Gaussian kernel, is a popular kernel function commonly used in SVM classification. It can map an input space in infinite dimensional space.

The equation for the [RBF kernel](https://en.wikipedia.org/wiki/Radial_basis_function_kernel) is:

K(x, x') = exp(-||x - x'||² / 2&sigma;²)

Where:
- K(x, x') is the RBF kernel (similarity score)
- γ (gamma) is a free parameter. It must be greater than 0.
- ||x - x'||² is the squared Euclidean distance between the two feature vectors.

The RBF kernel is a measure of similarity between x and x': if they are identical, the score is 1; if they are very dissimilar, the score is close to 0.