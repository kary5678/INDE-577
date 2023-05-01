# Dense Neural Networks

Dense neural networks (DNN) are a type of artificial neural network used for both classification and regression tasks. They are called "dense" because all nodes in one layer are fully connected to all nodes in the previous layer, creating a dense matrix of connections. One subset of dense neural networks is the multilayer perceptron.

A DNN consists of an input layer, one or more hidden layers, and an output layer. Each layer consists of a number of nodes (also called neurons) that perform computations on the input data. Each node in a layer receives input from all the nodes in the previous layer and applies a non-linear activation function to the weighted sum of the inputs. The weights and biases of each node are adjusted during training to minimize the loss function.

The number of nodes in the input layer is determined by the number of features in the input data, while the number of nodes in the output layer depends on the type of problem being solved. For example, a binary classification problem requires one node in the output layer to predict the probability of belonging to one of the two classes, but a multi-class classification problem requires a separate node for each class, each node representing the probability of belonging to that class. The number of hidden layers and the number of nodes in each layer are hyperparameters that need to be tuned during training. Deeper networks with more layers can learn more complex representations of the data but are more computationally expensive to train.

Examples of problems that can be solved using dense neural networks are image classification, object recognition, natural language processing, audio analysis, sentiment analysis, opinion mining, and computer vision. The range is vast; dense neural networks are versatile.

## Algorithm

1. Initialize the weights $\mathbf{W}$ and biases $\mathbf{b}$ randomly.

2. Feed the input data $\mathbf{x}$ into the network and propagate it through the layers to compute the output $\mathbf{y}$:

    $$\mathbf{a}^{(0)} = \mathbf{x}$$
    
    $$\mathbf{z}^{(l)} = \mathbf{W}^{(l)}\mathbf{a}^{(l-1)} + \mathbf{b}^{(l)}$$
    
    $$\mathbf{a}^{(l)} = \sigma(\mathbf{z}^{(l)})$$
    
    where $\mathbf{a}^{(l)}$ is the activation of the $l$-th layer, $\mathbf{W}^{(l)}$ and $\mathbf{b}^{(l)}$ are the weights and biases for that layer, and $\sigma(\cdot)$ is the activation function.

3. Compute the output of the last layer, which will be the predicted output $\hat{\mathbf{y}} = \mathbf{a}^{(L)}$, where $L$ is the number of layers in the network.

4. Calculate the loss between the predicted output and the actual output $\mathbf{y}$ using a loss function $J(\mathbf{W}, \mathbf{b})$:

    $$J(\mathbf{W}, \mathbf{b}) = \frac{1}{N} \sum_{i=1}^N L(\hat{\mathbf{y}}^{(i)}, \mathbf{y}^{(i)})$$
    
    where $N$ is the number of training examples, and $L(\cdot)$ is the loss function.

5. Compute the gradient of the loss function with respect to the weights and biases using backpropagation. This involves computing the error at each layer and propagating it backwards through the network to compute the gradients. The gradients are:

    $$\delta^{(L)} = \nabla_{\hat{\mathbf{y}}} J(\mathbf{W}, \mathbf{b}) \odot \sigma'(\mathbf{z}^{(L)})$$
    
    $$\delta^{(l)} = \left( (\mathbf{W}^{(l+1)})^\intercal \delta^{(l+1)} \right) \odot \sigma'(\mathbf{z}^{(l)})$$
    
    $$\nabla_{\mathbf{W}^{(l)}} J(\mathbf{W}, \mathbf{b}) = \delta^{(l)} (\mathbf{a}^{(l-1)})^\intercal$$
    
    $$\nabla_{\mathbf{b}^{(l)}} J(\mathbf{W}, \mathbf{b}) = \delta^{(l)}$$

6. Update the weights and biases using an optimization algorithm such as stochastic gradient descent or Adam:

    $$\mathbf{W}^{(l)} \leftarrow \mathbf{W}^{(l)} - \alpha \nabla_{\mathbf{W}^{(l)}} J(\mathbf{W}, \mathbf{b})$$
    
### Breaking it down

DNNs are trained using backpropagation, which is an iterative process of adjusting the weights and biases of the network based on the difference between the predicted output and the true output. The loss function used for training depends on the type of problem being solved. For example, a binary classification problem may use binary cross-entropy loss, while a regression problem may use mean squared error loss.

During training, the network updates its weights and biases based on the gradients of the loss function with respect to the parameters. The learning rate is a hyperparameter that determines the size of the steps taken during each update. Too high of a learning rate can cause the algorithm to overshoot the optimal weights and biases, while too low of a learning rate can result in slow convergence.

## Advantages/Disadvantages

✓ Can learn complex non-linear relationships between inputs and outputs

✓ Can automatically extract features from the data, reducing the need for manual feature engineering

✓ Can handle high-dimensional data and are scalable to large datasets

✗ Computationally expensive to train and require large amounts of data to prevent overfitting

✗ Prone to getting stuck in local minima during training

✗ Difficult to interpret, making it hard to understand how they arrived at a particular prediction

## Implementation on Dataset

A dense neural network is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/dense_neural_network/dense_neural_network.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
