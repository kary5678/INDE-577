# Logistic Regression

Logistic regression is a supervised machine learning technique used for binary classification problems. It is a statistical model that is used to estimate the probability of an instance belonging to a particular class, given its features. 

## Algorithm

1. For each $i=1, \dots, N$ in given labeled data $\{(\textbf{x}^1, y^1), (\textbf{x}^2, y^2), \dots, (\textbf{x}^N, y^N)\}$, feed $\textbf{x}^{(i)}$ into the model to predict $\hat{y}^{(i)}$:

    a. Calculate the weighted sum of the input features and bias term, $z = \textbf{x}^\intercal\textbf{w} + b$
    
    b. Pass the result through a sigmoid function $\sigma(z) = \frac{1}{1+e^{-z}}$, which returns a probability value between 0 and 1
    
    c. Choose a cutoff threshold for the probabilities, such as 0.5. If the probability value is greater than the cutoff value, predict the positive class, otherwise predict the negative class.
    
2. Update the model parameters by minimizing a cost function using an optimization algorithm such as gradient descent:

    a. Use the cross-entropy loss function, $J(\textbf{w}, b) = -\frac{1}{N}\sum\limits_{i=1}^{N}[y^{(i)}\log\hat{y}^{(i)} + (1-y^{(i)})\log(1-\hat{y}^{(i)})]$, to measure the difference between the predicted probability and the actual label.
    
    b. Update the weights and bias using the gradient descent algorithm, $\textbf{w} \leftarrow \textbf{w} - \alpha \nabla_{\textbf{w}}J$ and $b \leftarrow b - \alpha \nabla_{b}J$, where $\alpha$ is the learning rate and $\nabla_{\textbf{w}}J$ and $\nabla_{b}J$ are the partial derivatives of the cost function with respect to the weights and bias term, respectively.
    
3. Repeat step 1 and 2 until convergence, or until a maximum number of iterations is reached.

### Breaking it down

The logistic regression algorithm works by modeling the relationship between the input features and the binary output variable. It assumes that the log-odds of the positive class are linearly related to the input features:

$$\log\frac{P(y=1|\textbf{x})}{1-P(y=1|\textbf{x})} = \textbf{x}^\intercal\textbf{w} + b$$

$P(y=1|\textbf{x})$ is the probability of the positive class given the input features $\textbf{x}$, and $\textbf{w}$ and $b$ are the weight vector and bias term, respectively. The sigmoid function is then used to convert the log-odds to a probability value.

## Advantages/Disadvantages

✓ Simple and easy-to-understand

✓ Can handle both linear and nonlinear relationships between the input features and the output variable by using nonlinear transformations of the input features

✓ Provide useful insights into the relative importance of different input features for predicting the output class probabilities

✗ Assumes a linear relationship between the input features and the log-odds of the positive class

✗ Sensitive to outliers and irrelevant input features, which can lead to overfitting or poor performance on new data

✗ Can struggle with imbalanced datasets, where one class is much rarer than the other, and may require additional techniques such as oversampling, undersampling, or cost-sensitive learning

✗ Less flexible than other machine learning algorithms such as decision trees or neural networks, which are able to capture more complex and non-linear relationships between the input features and the output class probabilities

## Implementation on Dataset

The logistic regression algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/logistic_regression/logistic_regression.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features for this classification task can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
