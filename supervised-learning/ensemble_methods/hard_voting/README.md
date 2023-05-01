# Voting

Voting is a supervised machine learning technique used for classification or regression tasks. It is an ensemble method where multiple models are trained on the same dataset and their results are combined to give a final output.

## Regression Voting

In regression voting, the predicted values from each model are combined to give a final output. The simplest approach is to take the average of the predicted values from each model. However, more advanced methods can be used, such as weighted averaging, where the models' predictions are weighted based on their performance on a validation set. It's important to note that regression voting may not always lead to improved performance compared to using a single model, especially if the individual models have high variance.

## Classification Voting

In classification voting, the predicted classes from each model are combined to give a final output. The simplest approach is to use majority voting, where the class with the most votes is selected as the final output. However, other methods can be used, such as weighted voting, where each model's predictions are weighted based on their performance on a validation set. Voting leads to improved accuracy and robustness compared to using a single model. However, it may not always lead to improved performance, especially if the individual models have high correlation.

### Hard Voting

In hard voting, the output of each model is considered as a vote, and the class with the majority votes is chosen as the final output. This approach works best when the individual models have different biases and perform well on different parts of the dataset.

### Soft Voting

In soft voting, the probability estimates of each model are combined to calculate the weighted average probability for each class. The class with the highest probability is chosen as the final output. This approach works best when the models are well-calibrated and produce accurate probability estimates.

### Algorithm

1. For each $i=1, \dots, N$ in given labeled data $\{(\textbf{x}^1, y^1), (\textbf{x}^2, y^2), \dots, (\textbf{x}^N, y^N)\}$, train multiple models, each using a different algorithm or set of hyperparameters.

2. For each input instance $\textbf{x}$, obtain the predicted class probabilities from each model.

3. Combine the predicted class probabilities from each model using either hard or soft voting.

    a. For hard voting, choose the class with the majority vote as the final output.
    
    b. For soft voting, calculate the weighted average probability for each class and choose the class with the highest probability as the final output.

## Advantages/Disadvantages

✓ Can improve the accuracy of a single model by combining the strengths of multiple models

✓ Helps to reduce the risk of overfitting, especially when using different algorithms or subsets of the data

✓ Provides a simple and interpretable solution for classification problems

✗ Can be computationally expensive and slow, especially when using a large number of models

✗ Requires multiple models to be trained and stored, which can be challenging in resource-constrained environments

✗ Accuracy of the voting approach depends heavily on the quality of the individual models used

## Implementation on Dataset

The voting algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/ensemble_methods/hard_voting/voting.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
