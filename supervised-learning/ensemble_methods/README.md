# Ensemble Methods

Ensemble methods are a supervised machine learning technique that combines multiple models to improve the overall performance of a predictive model. The idea behind ensemble methods is that by combining the predictions of multiple models, the resulting model will be more accurate and robust than any individual model.

### Analogy 

In class, we watched a [video on guessing jellybeans in a jar](https://youtu.be/iOucwX7Z1HU). Imagine you are trying to guess the number of jellybeans in a jar. You take a look at the jar, try to estimate its size, and make a guess based on that information. However, you are not sure if your guess is accurate, as it's just based on your personal estimate.

Now imagine you are part of a group of people trying to guess the same thing. Each person in the group takes a look at the jar and makes their own guess based on their individual estimate. The group then combines all of the guesses together to come up with a final estimate. Even though each individual guess may not be perfect, the group's final estimate is likely to be more accurate than any single guess. This is because the group's estimate takes into account a wider range of estimates and individual perspectives, reducing the impact of any individual error or bias.

Similarly, in machine learning, ensemble methods combine multiple models that each have their own strengths and weaknesses. The resulting ensemble model is often more accurate and robust than any single model, as it takes into account a wider range of perspectives and can better capture the complexity of the data.

## Advantages/Disadvantages

✓ **Improved accuracy**: Can produce more accurate predictions than any individual model

✓ **Robustness**: More robust to noise and outliers in the data, since they consider multiple models rather than just one

✓ **Generalization**: Improves the generalization of the model, making it more likely to perform well on unseen data

✓ **Flexibility**: Can be used with a wide range of models, including linear and nonlinear models, decision trees, and neural networks

✗ **Complexity**: More complex than individual models, requiring more computational resources and longer training times

✗ **Overfitting**: Prone to overfitting if the individual models are overfitting the data

✗ **Interpretability**: Less interpretable than individual models, making it more difficult to understand how the model is making its predictions

## Directory Contents

I implement the following 4 ensemble methods in my repository:

1. [**Voting**](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/hard_voting) - aggregate outputs from multiple models to make predictions 

2. [**Bagging**](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/bagging) - train multiple models on different subsets of the training data and combine their predictions

3. [**Random Forests**](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/random_forests) - combine multiple decision trees to create a more accurate and robust model

4. [**Boosting**](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/ensemble_methods/boosting) - combines multiple weak classifiers to create a strong classifier
