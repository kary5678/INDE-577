# Cross Validation

Cross validation is a technique used in machine learning to evaluate the performance of a model by splitting the data into multiple subsets and training the model on different combinations of these subsets. The goal of cross validation is to test the generalization ability of a model and prevent overfitting by checking its performance on data that it has not seen before.

## Popular Techniques

There are several popular techniques for cross validation, including:

- ***k*-fold cross validation**: splitting the data into *k* subsets and using each subset as a validation set while training on the remaining $k-1$ subsets

- **Leave-one-out cross validation (LOOCV)**: using a single observation as the validation set while training on the remaining data

- **Stratified cross validation**: preserving the class distribution of the data while splitting it into subsets

- **Time-series cross validation**: splitting the data into time-based subsets to simulate real-world scenarios

- **Nested cross validation**: using one cross validation loop to evaluate the performance of the model and another to optimize its hyperparameters

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
