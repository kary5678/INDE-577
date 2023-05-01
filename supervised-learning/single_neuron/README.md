# The Single Neuron Model

The single neuron model is the building block of neural networks. The model takes a set of input values, computes a weighted sum of those inputs, adds a bias term, and applies an activation function to the result. The output of the activation function is the output of the neuron.

## Algorithm

1. For each $i=1, \dots, N$ in given labeled data $\{(\textbf{x}^1, y^1), (\textbf{x}^2, y^2), \dots, (\textbf{x}^N, y^N)\}$, feed $\textbf{x}^{(i)}$ into the model to predict $\hat{y}^{(i)}$. Then,

    a. Compute the weighted sum, $z=\textbf{x}^\intercal\textbf{w}+b$
    
    b. Apply the activation function, $h(z)$, to obtain the output of the neuron, $a=h(z)$
    
    c. Compute the neuron cost function, $C(\textbf{w}, b)$, which measures the difference between the predicted output and the true output.

2. Adjust the weights and bias based on the gradient of the cost function with respect to these parameters using an optimization algorithm such as gradient descent.

3. Repeat (1) and (2) until convergence or a stopping criterion is met.


### Activation Functions

By specifying different activation and cost functions, the single neuron acts as a perceptron, logistic regression, or linear regression model.

* **Perceptron**: sign function $sign(z)$, where $z$ is the weighted sum
* **Logistic regression**: sigmoid/logistic function $\frac{1}{1+e^{-z}}$, where $z$ is the weighted sum
* **Linear regression**: linear activation function $z$, where $z$ is the weighted sum


### Cost Functions

* **Perceptron**: MSE, $C(\textbf{w}, b)=\frac{1}{2N}\sum\limits_{i=1}^{N}(y^{(i)}-\textbf{w}^\intercal\textbf{x}^{(i)}-b)^2$
* **Logistic regression**: cross entropy, $C(\textbf{w}, b)=-\frac{1}{N}\sum\limits_{i=1}^{N}[y^{(i)}\log(a^{(i)})+(1-y^{(i)})\log(1-a^{(i)})]$
* **Linear regression**: MSE, $C(\textbf{w}, b)=\frac{1}{2N}\sum\limits_{i=1}^{N}(y^{(i)}-\textbf{w}^\intercal\textbf{x}^{(i)}-b)^2$


## Advantages/Disadvantages

✓ Relatively easy to interpret because of its simplicity

✓ Use of weights can give information about features, such as their importance

✓ Computationally efficient, especially when the dataset is small and especially compared to more complex neural network models

✗ Complications arise with non-linear data; the single neuron model can only learn linear decision boundaries

✗ May overfit the training data if it is too complex or the learning rate is too high

## Implementation on Dataset

The single neuron model discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/single_neuron/single_neuron.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
