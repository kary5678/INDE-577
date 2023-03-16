# The Perceptron

The Perceptron is a supervised machine learning technique for classification. Specifically, it is a single neural model for *binary* classification, meaning that it will identify which of two classes something is, given its feature inputs. 

The Perceptron dates back to 1957. Its inventor [Frank Rosenblatt](https://en.wikipedia.org/wiki/Frank_Rosenblatt) was an American psychologist notable in the field of artificial intelligence; he is sometimes called the father of deep learning.

## Algorithm

1. For each $i=1, \dots, N$ in given labeled data $\{(\textbf{x}^1, y^1), (\textbf{x}^2, y^2), \dots, (\textbf{x}^N, y^N)\}$, feed $\textbf{x}^{(i)}$ into the model to predict $\hat{y}^{(i)}$. Then,

    a. Perform the weight perceptron update rule, $\textbf{w} \leftarrow \textbf{w} - \frac{1}{2}(\hat{y}^{(i)}-{y}^{(i)})\textbf{x}^{(i)}$
    
    b. Perform the bias perceptron update rule, $b \leftarrow b - \frac{1}{2}(\hat{y}^{(i)}-{y}^{(i)})$

2. Repeat (1) until either
  
    a. the maximum number of *epochs* has been reached OR
  
    b. the cost function outputs a sufficiently small error
    
### Breaking it down

The simple explanation of the Perceptron has two steps. The Perceptron takes in numerical inputs associated with a weight, $w_j$, along with a bias term, $b$. The first step is to calculate a *weighted sum*:

$$z=w_1x_1 + w_2x_2 + \dots + w_nx_n + b = \textbf{x}^\intercal\textbf{w}$$

A **step function** or **activation function** is then applied to the weighted sum, z, outputting $h_{\textbf{w}}(\textbf{x})= step(z)=\phi(z)$. Step functions include the heaviside function or the sign function. The output of the step function is what classifies the inputted instance to either the positive or negative class.

Seems simple enough, but there's one problem. We don't know what the weights for the inputs are, or how they should be chosen!

The weights and bias term are initalized randomly, such as from a uniform distribution. They are then updated through a training/learning process based on performance metrics, such as the **neuron cost function**:

$$C(\textbf{w}, b)=\frac{1}{4}\sum_{i=1}^{N}(\hat{y}^{(i)}-{y}^{(i)})^2$$

TO-DO: define positive/negative class, bias, update rule

## Advantages/Disadvantages
✓ Simple, converges to a solution if training instances are linearly separable

✓ Relatively easy to interpret because of its simplicity

✓ Use of weights can give information about features, such as their importance

<br>
✗ Incapable of learning complex patterns given that decision boundaries are linear

## Implementation on Dataset

The Perceptron algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/perceptron/perceptron.ipynb) using the [Hawks](https://r-data.pmagunia.com/dataset/r-dataset-package-stat2data-hawks) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features for this classification task can be found in the notebook.
