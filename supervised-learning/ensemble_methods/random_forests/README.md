# Random Forests

The random forest is a supervised machine learning algorithm that is based on decision trees. It is used for both classification and regression tasks, and as an ensemble method, it is considered to be one of the most versatile and powerful machine learning techniques.

The random in "random forests" refers to the fact that each decision tree is constructed using a random subset of the data, as well as a random subset of the available features. This introduces a level of randomness into the algorithm, which helps to prevent overfitting and improve the accuracy of the final predictions.

## Algorithm

The random forest algorithm works by building a large number of decision trees and then combining their predictions to make a final prediction.

1. Randomly select a subset of the data (with replacement) and build a decision tree on that subset.

2. Repeat step 1 many times to create a forest of decision trees.

3. To make a prediction for a new instance, pass it through each of the decision trees in the forest and take a majority vote of the predictions.

## Advantages/Disadvantages

✓ Highly accurate and robust because they combine many decision trees, each with their own random subset of the data

✓ Can handle a large number of features and are not affected by irrelevant or redundant features

✓ Can provide an estimate of the importance of each feature in the classification/regression task

✗ Computationally expensive to train, especially with a large number of decision trees

✗ May not perform well on small datasets, since it is difficult to create a diverse set of decision trees with limited data

✗ Results can be difficult to interpret, since the final prediction is based on a combination of many decision trees

## Implementation on Dataset

The random forest algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/ensemble_methods/random_forests/random_forests.ipynb) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
