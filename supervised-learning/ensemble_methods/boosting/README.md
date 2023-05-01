# Boosting

Boosting is a supervised machine learning technique used for classification or regression tasks; specifically, boosting is an ensemble method that combines multiple weak learners to create a strong model. The term "weak learner" generally refers to a model that performs only slightly better than random guessing. Boosting sequentially trains weak models on different subsets of the training data, with each subsequent model placed more emphasis on data points that previous models have struggled with. This way, the final model is a weighted combination of all the weak models, with each model's weights determined by its performance on the training data.

## Algorithm

1. Initialize the weights for each data point in the training set to equal values.

2. Train a weak model on a subset of the training data using the current weights.

3. Evaluate the weak model's performance on the entire training set.

4. Increase the weights of data points that the weak model misclassified.

5. Normalize the weights so that they sum to one.

6. Repeat steps 2-5 for a predetermined number of iterations or until the error on the training set reaches a satisfactory level.

7. Combine the weak models into a single strong model, with the weights of each weak model determined by its performance on the training data.

## Advantages/Disadvantages

✓ Can be used with a wide variety of weak models including decision trees, neural networks, and support vector machines

✓ Can improve the performance of weak models, allowing them to make more accurate predictions

✓ Can handle noisy or imbalanced data sets, as it places more emphasis on misclassified data points

✗ Computationally expensive, as it trains multiple models sequentially

✗ Prone to overfitting if the weak models are too complex or the number of iterations is too high

✗ Sensitive to outliers in the training data, as these data points may receive high weights and bias the model towards them

## Implementation on Dataset

The boosting algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/ensemble_methods/boosting/boosting.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
