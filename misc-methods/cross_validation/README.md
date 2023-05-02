# Cross Validation

Cross validation is a technique used in machine learning to evaluate the performance of a model by splitting the data into multiple subsets and training the model on different combinations of these subsets. The goal of cross validation is to test the generalization ability of a model and prevent overfitting by checking its performance on data that it has not seen before. 

Some examples of cross validation techniques are ***k*-fold cross validation** (splitting the data into *k* subsets and using each subset as a validation set while training on the remaining $k-1$ subsets) and **leave-one-out cross validation (LOOCV)** (using a single observation as the validation set while training on the remaining data).

## Algorithm (*k*-fold cross validation)

1. Split the dataset into k equal-sized folds
2. For each fold i from 1 to k:

    2a. Use fold i as the validation set and the remaining k-1 folds as the training set
  
    2b. Train the model on the training set and evaluate it on the validation set
  
    2c. Record the evaluation metric(s) for the current fold i
  
3. Compute the average evaluation metric(s) across all k folds

By averaging the evaluation metric(s) across all k folds, we can obtain a more reliable estimate of the model's performance than if we only evaluated it on a single train-test split. Example of evaluation metrics are accuracy, precision, and recall (for classification problems) or mean squared error (for regression problems).

## Advantages/Disadvantages

✓ Prevents overfitting by testing the model's performance on data that it has not seen before

✓ Allows for the evaluation of the model's generalization ability, which is important for its practical application

✓ Provides a way to compare different models and feature selection methods

✓ Can be used to optimize hyperparameters and improve model performance

✗ Can be computationally expensive, especially for large datasets or complex models

✗ May lead to bias if the data is not representative of the underlying distribution

✗ Can be sensitive to the choice of validation technique and the number of folds

## Implementation on Dataset

Cross validation is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/misc-methods/cross_validation/cross_validation.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
