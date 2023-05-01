# Decision Trees

Decision trees are a popular supervised machine learning technique for both classification and regression problems. They use a tree-like model of decisions and their possible consequences, including chance events and resource costs, to predict the outcome of a decision. The model can be used to solve problems in which the decision is based on a set of observed features or predictors.

Decision trees are a hierarchical model composed of nodes that represent decision rules and leaves that represent the class labels. The top node of a decision tree is called the *root* node, which represents the entire dataset. The nodes in a decision tree are typically classified into two types: *internal* nodes and *leaf* nodes. Internal nodes, also known as "decision nodes", are nodes that represent decision criteria or tests on one of the input features. They have one incoming edge from a *parent* node and one or more outgoing edges that lead to *child* nodes. Leaf nodes, also known as "terminal nodes", are nodes that represent a final decision or classification for each data point. They have one incoming edge from a parent node but no outgoing edges.

## Algorithm

1. Choose the best attribute for splitting the data into subsets.
2. Create a new node in the tree with the chosen attribute as a decision point.
3. Split the data into subsets based on the value of the chosen attribute.
4. Recursively repeat the process on each subset until a stopping criterion is met, such as reaching a certain depth or having a minimum number of instances in the subset.
5. Assign a class label to the leaf node based on the majority class of instances in that subset.

### Breaking it down

The basic idea of decision trees is to partition the feature space into rectangular regions, with each region corresponding to a specific class. The algorithm chooses the attribute that best splits the data, according to some criterion, such as the Gini index or information gain.

* The Gini index measures the probability of misclassifying an instance in a random subset.
* The information gain measures the expected reduction in entropy, or uncertainty, in the subset after the split.

The split is chosen to maximize the difference in purity between the subsets of instances created by the split. The purity of a subset is measured by the proportion of instances in that subset that belong to a particular class. The algorithm then recursively repeats the process on each subset until a stopping criterion is met. This generates a tree-like model of decisions and their possible consequences.

Some hyperparameters to consider in optimizing a decision tree are:

* Maximum depth: a deeper tree can fit more complex relationships in the data but may overfit to the training data
* Minimum sample split: a higher value for the minimum number of samples required to split an internal node helps to prevent overfitting but may result in a simpler model
* Minimum sample leaf: A higher value for the minimum number of samples required to be at a leaf node helps to prevent overfitting but may result in a simpler model.
* Maximum features: a lower value of the number of features to consider when looking for the best split can reduce overfitting but may result in a less accurate model

## Advantages/Disadvantages

✓ Easy to understand and interpret, as they can be visualized and explained easily

✓ Capable of handling both categorical and continuous data.

✓ Can handle missing data by making decisions based on the available data

✓ Can be used for feature selection by ranking the importance of features based on their contribution to the tree

✗ Prone to overfitting (which can be mitigated by setting stopping criteria, pruning the tree, or using ensemble methods)

✗ Sensitive to noise in the data, which can lead to the creation of spurious splits

✗ Can be biased towards attributes with many levels or categories, resulting in overrepresentation of certain features

## Implementation on Dataset

The decision tree algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/decision_trees/decision_trees.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
