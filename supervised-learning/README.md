# Supervised Learning

In supervised learning, the training dataset includes labels for each data point. While the ultimate goal is to have a model that makes predictions given inputs, having labeled training data is a form of feedback in the learning process and can make it faster to train a model compared to unsupervised learning tasks.

Two common supervised learning tasks are *classification* and *regression*. Classification involves outputs that are discrete categories, while regression generally involves outputs that are continuous, numerical quantities.

### Classification Tasks

If the goal is to categorize based on features, then classification is the appropriate task. In classification, a class label is obtained from input data. 

Some examples of classification tasks include:

* using sepal width or petal length to predict if an iris is the setosa or versicolor species
* classifying emails as spam or not spam

### Regression Tasks

In regression, a set of features, predictors, are used to predict a target *numeric* value. 

Some examples of regression tasks include:

* predicting health insurance costs given predictors
* predicting college admission given test scores

**Note:** Some regression algorithms can be used for classification tasks, such as logistic regression!

## Directory Contents

To learn more about each algorithm and see them in application, visit their respective linked subdirectories.

**Parametric models**

1. [The Perceptron](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/perceptron) - for binary classification tasks
2. [Linear Regression](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/linear_regression) - for regression tasks
3. [Logistic Regression](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/logistic_regression) - for binary classification tasks
4. [The Single Neuron Model](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/single_neuron) - encompasses the perceptron, linear regression, logistic regression, etc.
5. [Dense Neural Networks](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/dense_neural_network)

**Nonparametric models**

6. [k-Nearest Neighbors](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/knn)
7. [Decision Trees](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/decision_trees)
