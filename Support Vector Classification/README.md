# README.md

## Support Vector Classification (SVC)

Support Vector Classification (SVC) is a type of Support Vector Machine (SVM) that is commonly used in machine learning for classification tasks. It is a supervised learning model that uses a technique called the kernel trick to transform your data and then based on these transformations it finds an optimal boundary between the possible outputs.

### How it Works

SVC works by finding a hyperplane that best divides the dataset into classes. The hyperplane is chosen to maximize the margin between the classes in the dataset. The vectors (or data points) that define the hyperplane are the support vectors. 

In a two-dimensional space, this hyperplane is a line dividing a plane into two parts where each class lay on either side. The goal of SVC is to choose a hyperplane with the greatest possible margin between the hyperplane and any point within the training set, giving a greater chance of new data being classified correctly.

### How it's Calculated

The calculation of SVC involves a few steps:

1. **Training**: During the training phase, the algorithm takes in a set of input data and outputs a trained model. In the case of a linear SVC, the output is a hyperplane that separates the classes as best as possible.

2. **Classification**: During the classification phase, the algorithm takes in new unseen input data and uses the trained model to predict the output. The unseen data is plotted with respect to the hyperplane. If the data falls on one side of the hyperplane, it's classified as one class, and if it falls on the other side, it's classified as the other class.

### When to Use SVC

SVC is a powerful algorithm that works well on a wide range of classification tasks. Here are a few situations where SVC is particularly useful:

- **High Dimensional Spaces**: SVC is effective in high dimensional spaces, and it's still effective when the number of dimensions is greater than the number of samples.

- **Complex Domains**: SVC can model complex relationships using custom kernels.

- **Clear Margin of Separation**: SVC works best when there is a clear margin of separation between classes.

However, SVC is not suitable for large datasets because the training time with SVC can be high compared to other algorithms. It also doesn't perform well when the dataset has more noise i.e. target classes are overlapping.

---

This project uses the Support Vector Classification to classify a dataset of social network ads. The dataset contains information about users, and the model predicts whether a user will purchase a product or not based on their age and estimated salary. The SVC model is trained on a subset of the data and then used to make predictions on unseen data. The performance of the model is evaluated using a confusion matrix and accuracy score.