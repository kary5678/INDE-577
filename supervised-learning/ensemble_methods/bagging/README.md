# Bagging

Bagging (bootstrap aggregating) is a supervised machine learning technique used for classification or regression tasks. It is an ensemble method that combines multiple models to improve the overall accuracy and stability of predictions. One example is decision tree bagging, otherwise known as random forests.

## Algorithm

1. Create multiple subsamples of the original training data, each of size n, by sampling with replacement from the original data. 

2. Train a base model (e.g., decision tree, neural network, etc.) on each subsample of the training data.

3. For a new instance, predict using all the trained models and then aggregate the predictions using a voting or averaging approach.

## Advantages/Disadvantages

✓ Reduces variance and overfitting by combining multiple models

✓ Can improve prediction accuracy when the base models are weak

✓ Handles imbalanced classes well

✗ Can lead to increased bias if the base models are too similar

✗ May not improve performance if the base models are already accurate and diverse

✗ Requires additional computational resources to train and store multiple models

## Implementation on Dataset

The bagging algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/ensemble_methods/bagging/bagging.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
