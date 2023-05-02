# Miscellaneous Methods

In this directory, I demonstrate some good machine learning practices that can be used to improve model performance. This will just be a collection of tools to keep in the back of one's mind when fitting a machine learning model.

## Directory Contents

To learn more about each method and see them in application, visit their respective linked subdirectories.

1. [**Cross validation**](https://github.com/kary5678/INDE-577/tree/main/misc-methods/cross_validation) - evaluating the generalized performance of a model

2. [**Feature selection**](https://github.com/kary5678/INDE-577/tree/main/misc-methods/feature_selection) - removing irrelevant or redundant features

3. [**Random oversampling & random undersampling**](https://github.com/kary5678/INDE-577/tree/main/misc-methods/random_oversampling) - addressing class imbalance and bias towards the majority class

---

In addition, I will take this time to emphasize that the best machine learning model depends on what question/task you set out to solve. For example, accuracy isn't a blanket metric in showing that a particular model is better over another - you can have high accuracy, but all the misclassifications are in the minority class that is difficult to understand the pattern of. In the next section, I will outline some other useful metrics and their interpretations.

## Common Performance Metrics

### Classification

- **Accuracy**: Ratio of correct predictions to the total number of predictions made

- **Precision**: Measure of how many of the positive predictions made by the classifier are actually correct
  - Calculated as the ratio of true positives (TP) to the sum of true positives and false positives (FP) 
  - A high precision score indicates that the classifier has a low false positive rate and is not making many incorrect positive predictions
  - Out of all the observations that the model predicts is a given class, what percentage actually were?

- **Recall**: Measure of how many of the actual positive instances in the dataset were correctly identified by the classifier 
  - Calculated as the ratio of true positives to the sum of true positives and false negatives (FN)
  - A high recall score indicates that the classifier has a low false negative rate and is not missing many positive instances
  - Out of all the observations that actually were a given class, what percentage of these observations did the model predict correctly?

- **F1 score**: Measure that combines both precision and recall into a single score
  - Calculated as the harmonic mean of precision and recall
  - Ranges from 0 to 1, with a higher score indicating better performance
  - Useful when the distribution of positive and negative instances in the dataset is uneven, as it provides a balance between precision and recall

### Regression

- **Mean squared error (MSE)**: Average of the squared differences between the predicted and actual values

- **Coefficient of determination ($R^2$)**: Proportion of the variance in the target variable that is explained by the independent variables
    - Ranging from 0-1, $R^2=1$ indicates a perfect fit while $R^2=0$ indicates that the model does not explain any of the variance in the target variable
    
## Common Machine Learning Dilemmas

- **Bias-variance tradeoff**: A model must balance its ability to fit the training data closely (low bias) with its ability to generalize to new, unseen data (low variance). Models with high bias tend to underfit the data, while models with high variance tend to overfit the data.

- **Overfitting vs. underfitting**: Overfitting occurs when a model is too complex and fits the training data too closely, to the point where it starts to capture noise rather than signal, while underfitting occurs when a model is too simple and cannot capture the underlying patterns in the data. Finding the right balance between complexity and simplicity is key to avoiding both overfitting and underfitting.

- **Model interpretability vs. performance**: Some models may be highly accurate but difficult to interpret, while others may be more interpretable but less accurate. This is a common dilemma in domains where transparency and accountability are important, such as healthcare or finance.
