# README.md

## K-Nearest Neighbors Classification (KNN)

K-Nearest Neighbors (KNN) is a type of instance-based learning algorithm that is used for both classification and regression tasks. However, it is more widely used in classification problems in the industry. KNN is a non-parametric, lazy learning algorithm. Non-parametric means there is no assumption for underlying data distribution and lazy algorithm means it does not need any training data points for model generation. All training data used in the testing phase. 

### How it Works

KNN works by finding the distances between a query and all the examples in the data, selecting the specified number examples (K) closest to the query, then votes for the most frequent label (in the case of classification) or averages the labels (in the case of regression).

### How it's Calculated

The calculation of KNN involves a few steps:

1. **Training**: During the training phase, the algorithm takes in a set of input data and outputs a trained model. In the case of KNN, the output is the set of labels for the training data.

2. **Classification**: During the classification phase, the algorithm takes in new unseen input data and uses the trained model to predict the output. The unseen data is compared with the training data, and the algorithm looks for the K nearest neighbors and classifies the new data point based on the majority of nearest neighbors.

### When to Use KNN

KNN is a simple algorithm that works well on a wide range of classification tasks. Here are a few situations where KNN is particularly useful:

- **Small Datasets**: KNN is a good choice when the dataset is small and the speed of classification is not an issue.

- **Multi-class Problems**: KNN can be used for multi-class classification problems where a data point can belong to more than one class.

- **Simple Prototype**: KNN is a good choice for a simple prototype where you want to classify data points without investing too much time in model training.

However, KNN is not suitable for large datasets because the prediction phase can be slow. It also doesn't perform well when the dataset has many dimensions (features).

---

This project uses the K-Nearest Neighbors Classification to classify a dataset of social network ads. The dataset contains information about users, and the model predicts whether a user will purchase a product or not based on their age and estimated salary. The KNN model is trained on a subset of the data and then used to make predictions on unseen data. The performance of the model is evaluated using a confusion matrix and accuracy score.