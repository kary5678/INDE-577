# *k*-Means Clustering

An unsupervised learning method, *k*-means clustering is an iterative process of assigning each data point to groups, slowly clustering data points based on similar features. The objective is to minimize the sum of distances between the data points and the cluster centroid, to identify the correct group each data point should belong to.

The standard *k*-means clustering algorithm was first proposed by Stuart Lloyd of Bell Labs in 1957 as a technique for pulse-code modulation, but the idea for *k*-means goes back to Hugo Steinhaus in 1956. 

## Algorithm

0. Normalize/scale the data appropriately, if desired. This will ensure that all features contribute equally to the distance calculations used in the clustering algorithm.
1. Choose $k \ge 1$. See the section below on how to choose an optimal value for *k*, the number of clusters you want to form in the dataset.
2. Place k centroids on the feature space. Specifically, randomly initialize k centroids on the feature space.
3. Assign each data point to a centroid, specifically the nearest one, based on the distance metric used (ex: Euclidean distance).
4. Update/reposition the centroids by assigning them to the average of all the points assigned to the respective cluster. 
5. Repeat steps 3-4 until the clusters stop moving or a maximum number of iterations is reached.

### Choosing *k*

The first step is to determine the value of *k* that is most appropriate. This can be determined by methods such as the elbow method or silhouette analysis.

* The elbow method involves plotting a heuretic such as inertia as a function of the number of clusters *k* and identifying the elbow point, which is the value of *k* where the rate of change slows down. The elbow point represents the optimal value of *k* where adding more clusters does not significantly improve the clustering performance.

* Inertia is a metric used to evaluate the quality of clustering results by measuring the sum of squared distances between each data point and its assigned centroid, across all clusters. Inertia can be thought of as a measure of how compact the clusters are, with lower values indicating more compact clusters. Increasing *k* will always decrease the inertia, so it's recommended that inertia is used in conjunction with other metrics (like the elbow method) to determine the optimal value of *k*.

* In silhouette analysis, calculate the silhouette score for different values of k. The silhouette score is a metric that measures how well each data point belongs to its assigned cluster compared to other clusters. Ranging from -1 to 1, a silhouette score closer to 1 indicates a better clustering.

In addition, consider the complexity problems with regard to small versus large values of *k*:

* Small values of *k* in *k*-means clustering can lead to overfitting, as we'd end up with larger and less homogeneous clusters. The model is too simple to capture the underlying structure of the data, resulting in poor clustering performance.

* Large values of *k* in *k*-means clustering can lead to underfitting. The number of clusters is increased, which can result in smaller and more homogeneous clusters containing very few data points. In this case, the model may fail to capture the underlying patterns and will have difficulties generalizing to new data.


## Advantages/Disadvantages
✓ Relatively fast and scalable algorithm that can handle large datasets with high dimensionalities.

✓ Easy to understand and interpret - results are in the form of cluster centroids, providing insights into underlying patterns in the data

✓ Can handle noise and outliers in the data to some extent, and is relatively robust to initialization

✗ Sensitive to initial conditions; can converge to sub-optimal solutions if the initial centroids are poorly placed

✗ Selecting the number of clusters, *k*, is not always straightforward and can have a significant impact on the quality of the results

✗ Assumes that the clusters are spherical and have equal variances, which may not be true

✗ Poor performance with non-linearly separable data

✗ Lack of robustness to extreme outliers/noise

## Implementation on Dataset

The *k*-means clustering algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/unsupervised-learning/k-means_clustering/k-means_clustering.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features for this classification task can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).

Since *k*-means clustering is an unsupervised learning method, the species labels are ignored. However, since I have them, I might as well use them to my advantage to understand how *k*-means clustering clusters the data, accounting for noise.
