# Decision Tree Regression

Decision Tree Regression is a machine learning algorithm that uses a decision tree model for predicting a value, which can be considered as a regression problem. It's a type of regression that uses tree-like model of decisions.

## How it Works

The decision tree regression model works by partitioning the input space into non-overlapping regions. For every input in the same region, the model outputs a constant value. This constant value is the mean target value for the training instances that fall into this region. The decision of making partitions is based on minimizing a set criterion.

The decision tree starts with a single node, which branches off into possible outcomes. Each of these outcomes leads to additional nodes, which branch off into other possibilities. This continues until a decision is made. The final decision is made by taking the mean of the terminal node (leaf node) the input has landed.

## About the Code

The provided code is a simple implementation of a Decision Tree Regression model using Python and the Scikit-learn library. The code reads a dataset from a CSV file, 'Position_Salaries.csv', and splits it into features (X) and target variable (y).

The model is then trained using the `DecisionTreeRegressor` class from Scikit-learn. The model is fitted with the features and target variable. A prediction is made for the input value of 6.5.

Finally, the results are visualized using matplotlib. The actual values are plotted as red points and the predicted values are plotted as a blue line. The title, x-label, and y-label are set for the plot and the plot is displayed.