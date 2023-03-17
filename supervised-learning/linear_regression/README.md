# Linear Regression

Linear regression is a supervised machine learning technique for regression, as the name implies. Specifically, it is a single neural model where a set of features, predictors, are used to predict a target numeric value.

$$y=\alpha + \beta_1x_1 + \beta_2x_2 + \dots + \beta_px_p $$

## Algorithm

1. Initialize model parameters, with are the *slope* coefficients and *intercept* of the line.

2. Calculate error using the cost/loss function.
    * See examples of cost functions below [here.]()

3. Calculate the gradient of the loss funciton with respect to the training data for each parameter.

4. Update the model parameters

    a. Update the weights, $\textbf{w} \leftarrow \textbf{w} - \frac{1}{2}(\hat{y}^{(i)}-{y}^{(i)})\textbf{x}^{(i)}$
    
    b. Update the bias, $b \leftarrow b - \frac{1}{2}(\hat{y}^{(i)}-{y}^{(i)})$
    
    c. TO-DO: fix this!!

5. Repeat (2)-(4) until either
  
    a. the maximum number of *epochs* has been reached OR
  
    b. the cost function outputs a sufficiently small error
    
### Breaking it down

### Performance Metrics

* Mean squared error (MSE): $C(\textbf{w}, b)=\frac{1}{2N}\sum_{i=1}^{N}(\hat{y}^{(i)}-{y}^{(i)})^2$
* Root mean squared error (RMSE)

## Advantages/Disadvantages

✓ Relatively easy to interpret because of its simplicity

✓ Use of weights can give information about features, such as their importance

<br>
✗ Complications arise with non-linear data

## Implementation on Dataset
