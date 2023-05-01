# INDE 577: Data Science & Machine Learning

This repository hosts code for a data science and machine learning course. Concepts are illustrated in Jupyter notebooks applying relevant algorithms on a dataset. The algorithms include both supervised methods for classification and regression, as well as unsupervised learning methods.

## Contents

The algorithms enumerated below are each organized into their own subdirectory containing a `README.md` explanation of relevant background and a `.ipynb` Jupyter notebook of code. To learn more about each algorithm and see them in application, visit their respective linked subdirectories.

### __**[Supervised Learning Methods](https://github.com/kary5678/INDE-577/tree/main/supervised-learning)**__ - classification & regression tasks on labeled data
1. [The Perceptron](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/perceptron) - binary classification task
2. [Linear Regression](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/linear_regression) - regression task
3. [Logistic Regression](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/logistic_regression) - binary classification task based on probability of belonging to the positive class
4. [The Single Neuron Model](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/single_neuron) - encompasses the perceptron, linear regression, logistic regression, etc.
5. [Dense Neural Networks](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/dense_neural_network) - network of interconnected layers learns complex relationships for both classification and regression tasks
6. [k-Nearest Neighbors](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/knn) - nonparametric method for both classification and regression tasks based on similarities existing in proximity
7. [Decision Trees](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/decision_trees) - nonparametric method for both classification and regression tasks based on a hierarchical tree-like model of decisions 
8. [Ensemble Methods](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods) - combine multiple models to improve the overall performance of a predictive model

   8a. [Voting](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/hard_voting) - aggregate outputs from multiple models to make predictions
   
   8b. [Bagging](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/bagging) - train multiple models on different subsets of the training data and combine their predictions
   
   8b. [Random Forests](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/random_forests) - combine multiple decision trees to create a more accurate and robust model
   
   8d. [Boosting](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/boosting) - combine multiple weak learners to create a stronger and more robust predictor
   
There is also a subdirectory hosting code from a [class exercise finding the best classifier for a stroke dataset](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/class_exercise_3-31). This exercise implements many of these supervised learning methods for classification and compares them.


### __**[Unsupervised Learning](https://github.com/kary5678/INDE-577/tree/main/unsupervised-learning)**__ - clustering & dimensionality reduction tasks on unlabeled data
1. [k-Means Clustering](https://github.com/kary5678/INDE-577/tree/main/unsupervised-learning/k-means_clustering) - clustering task
2. [Density-Based Spatial Clustering of Applications With Noise](https://github.com/kary5678/INDE-577/tree/main/unsupervised-learning/dbscan) - clustering task that accounts for noise/outliers
3. [Principal Component Analysis](https://github.com/kary5678/INDE-577/tree/main/unsupervised-learning/pca) - dimensionality reduction task

## Data
The datasets used are located in the [**Data**](https://github.com/kary5678/INDE-577/tree/main/Data) directory. The main dataset used is the Hawks dataset, which contains observations of three different hawk species and associated features such as wing length, tail length, body weight, etc. 

Please visit the directory for detailed descriptions about the data and appropriate visualizations.

## Software

Here are some of the tools used in this repository. You can also view the `requirements.txt` for a more comprehensive list of dependencies.

* [Anaconda Distribution](https://www.anaconda.com/products/distribution)
* Python 3.9.13
  * matplotlib
  * numpy
  * pandas
  * seaborn
  * scikit-learn/sklearn
  * tensorflow

## References/Resources
* *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (2nd Edition) by Aurélien Géron
* [Dr. Davila's GitHub repository](https://github.com/RandyRDavila/Data_Science_and_Machine_Learning_Spring_2022)
* [Dr. Davila's YouTube lectures](https://youtube.com/playlist?list=PLiUo37D6MN3Fc-lICEHyR46VfwynkIRrf)
