# Linear Regression

Linear regression is a supervised machine learning technique for regression, as the name implies. Specifically, it is a single neural model where a set of features, predictors, are used to predict a target numeric value. A typical linear regression line for $p$ predictors and intercept/bias term $\alpha$ can be written as:

$$y=\alpha + \beta_1x_1 + \beta_2x_2 + \dots + \beta_px_p $$

## Algorithm

1. Initialize model parameters, with are the *slope* coefficients and *intercept/bias* of the line.

2. Calculate error using the cost/loss function.
    * See examples of cost functions below [here.]()

3. Calculate the gradient of the loss funciton with respect to the training data for each parameter.

4. Update the model parameters. The hyperparameter $\eta$ is the learning rate, which determines how much the model parameters are updated in each iteration.

    a. Update the intercept, $\alpha \leftarrow \alpha - \eta\frac{\partial C}{\partial \alpha}$

    b. Update the slopes, $\beta_j \leftarrow \beta_j - \eta\frac{\partial C}{\partial \beta_j}$ for each feature $j$


5. Repeat (2)-(4) until either
  
    a. the maximum number of *epochs* has been reached OR
  
    b. the cost function outputs a sufficiently small error
    
### Breaking it down

In linear regression, the goal is to find the line of best fit that minimizes the distance between the predicted values and the actual values. This is achieved by minimizing a cost function, such as the mean squared error (MSE), which measures the average squared difference between the predicted and actual values.

To minimize the cost function, the algorithm adjusts the model parameters (slope coefficients and intercept/bias) by calculating the gradient of the cost function with respect to the parameters and updating them using a learning rate. This process is repeated until the cost function converges to a minimum or a maximum number of iterations is reached.

### Performance Metrics

* Mean squared error (MSE):  average squared difference between the predicted and actual values, $C(\alpha, \textbf{B})=\frac{1}{2N} \sum\limits_{i=1}^{N}(\hat{y}^{(i)}-{y}^{(i)})^2$
* Root mean squared error (RMSE): square root of the MSE, provides a measure of the standard deviation of the errors



## Advantages/Disadvantages

✓ Relatively easy to interpret because of its simplicity

✓ Use of weights can give information about features, such as their importance

✓ Computationally efficient, especially when the dataset is small

✗ Complications arise with non-linear data; linear regression assumes a linear relationship between the features and the target variable

✗ Sensitive to outliers

✗ Assumes that the errors are normally distributed and have constant variance

## Implementation on Dataset

The linear regression algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/linear_regression/linear_regression.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb). Since the task is regression, the ouput will need to be continuous/numerical, so I try to predict a hawk's weight given their other physical features.
