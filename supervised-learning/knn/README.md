# *k*-Nearest Neighbors

*k*-nearest neighbors, abbreviated as kNN, is a nonparametric supervised learning method based on the idea that similar data points are grouped together and close in proximity. This algorithm is able to perform both regression and classification.

kNN was first developed in 1951 by [Evelyn Fix](https://en.wikipedia.org/wiki/Evelyn_Fix) and [Joseph Hodges](https://en.wikipedia.org/wiki/Joseph_Lawson_Hodges_Jr.), two statisticians at the University of California, Berkeley. It was later expanded by Thomas Cover.

## Algorithm

1. Prepare the data
2. Choose k, which represents the number of neighbors
3. For each example in the data
 - 3.1 Calculate the distance between the query example and the current example from the data.
 - 3.2 Add the distance and the index of the example to an ordered collection
4. Sort the ordered collection of distances and indices from smallest to largest (in ascending order) by the distances
5. Pick the first K entries from the sorted collection
6. Get the labels of the selected K entries
7. If regression, return the mean of the K labels
8. If classification, return the mode of the K labels

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
