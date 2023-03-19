# *k*-Nearest Neighbors

*k*-nearest neighbors, abbreviated as kNN, is a nonparametric supervised learning method based on the idea that similar data points are grouped together and close in proximity. This algorithm is able to perform both regression and classification.

An example of kNN in usage could be a recommender system. For example, given information about music, you could find the *k*-nearest neighbors for a song and recommend them to a user. Of course, this concept is very preliminary!

kNN was first developed in 1951 by [Evelyn Fix](https://en.wikipedia.org/wiki/Evelyn_Fix) and [Joseph Hodges](https://en.wikipedia.org/wiki/Joseph_Lawson_Hodges_Jr.), two statisticians at the University of California, Berkeley. It was later expanded by Thomas Cover.

## Algorithm

To predict a target label for a given point, which I will denote as $\textbf{p}$, perform the following:
1. Prepare the training and testing data.
2. Choose *k*, which represents the number of neighbors. Read the ["Choosing *k*"](https://github.com/kary5678/INDE-577/tree/main/supervised-learning/knn#choosing-k) section below for more details on this.
3. For each example, $\textbf{q}_i$, in the training data ($i=1, \dots, n$):

    a. Calculate the distance between the $\textbf{p}$ and $\textbf{q}_i$. This can be done using the Euclidean distance:
    
    $$d(p, q) = \sqrt{(p-q)^\intercal(p-q)}$$
    
    b. Add the distance and $\textbf{q}_i$ (for convenience, its index) to an ordered collection
    
4. Sort the ordered collection of distances and indices, by smallest to largest distance
5. Pick the first *k* entries from the sorted collection - these are the entries that are the *k* closest neighbors to $\textbf{p}$
6. Get the labels of the selected *k* entries
7. Determine the label of $\textbf{p}$ based on the labels in (6)

    a. For regression tasks, return the mean of the *k* labels
    
    b. For classification, return the mode of the *k* labels

### Choosing *k*

The first step is to determine the value of *k* that is most appropriate. This can be determined by trying a set of *k*'s and determining which produces the least error, but also keeping into account the following:

* Small values of *k* can lead to overfitting and higher influences of noise in the data
* Large values of *k* are computationally expensive and can lead to underfitting
* Even values of *k* cause complications when ties arise

A widely accepted optimal value for *k* is $\sqrt n$, where *n* is the number of training samples.

## Advantages/Disadvantages
✓ Simple, easy to implement

✓ As a nonparametric method, it is flexible and minimizes assumptions about the data

✓ No need to build a model and tune several parameters

✓ Versatile - can be used for regression, classification, and search
<br></br>
✗ As a nonparametric method, it can be slow and require large amounts of data

✗ Significantly slower as the number of examples and/or predictors increase

## Implementation on Dataset

The *k*-nearest neighbors algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/supervised-learning/knn/knn.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks and features such as age, sex, wing length, body weight, tail length, etc. Using these features, I use kNN to predict a hawk's species. More details about this dataset and visualizations of the relevant features for this classification task can be found in the notebook.
