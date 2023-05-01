# DBSCAN: Density-Based Spatial Clustering of Applications With Noise

Density-based spatial clustering of applications with noise, or DBSCAN for short, first proposed in 1996 by Martin Ester, Hans-Peter Kriegel, Jörg Sander, and Xiaowei Xu. DBSCAN is an unsupervised learning method; it is a density-based clustering non-parametric algorithm. Given a set of points in some space, DBSCAN groups together points that are closely packed together (points with many nearby neighbors) while marking points that lie alone in low-density regions (nearest neighbors are too far away) as outliers.

Overall, DBSCAN is a versatile clustering algorithm that can be applied in a wide range of applications where identifying groups or patterns in data is useful, such as:

* Anomaly detection: DBSCAN can be used to identify outliers or anomalies in data, which can be useful in fraud detection, intrusion detection, or other security applications.

* Image segmentation: DBSCAN can be used to segment images based on pixel similarity, which can be useful in computer vision and image processing applications.

* Clustering geographic data: DBSCAN can be used to cluster geographic data based on location, such as identifying areas with high concentrations of crime or disease outbreaks.

* Recommender systems: DBSCAN can be used to cluster similar items or products based on customer purchase histories or other features, which can be used to make personalized recommendations to users.

* Sensor networks: DBSCAN can be used to detect anomalies or outliers in sensor data, which can be useful in environmental monitoring or other applications where sensors are used to collect data.


## How is DBSCAN different from *k*-means clustering?

* DBSCAN is a density-based clustering algorithm, while k-means is a centroid-based algorithm.
* DBSCAN does not require the number of clusters to be specified beforehand, while k-means requires the number of clusters to be specified as a hyperparameter.
* DBSCAN can handle clusters of different shapes and sizes, while k-means assumes that all clusters are spherical and equally sized.
* DBSCAN can identify noise points and outliers, while k-means assigns all points to a cluster, even if they don't belong to any meaningful cluster.
* DBSCAN is computationally efficient for large datasets, while k-means can be slow and computationally expensive for large datasets or high-dimensional data.

## Algorithm

1. Choose $\epsilon>0$ and $N \ge 1$. The choice of $\epsilon$ and $N$ will have a significant impact on the resulting clustering, so make sure to choose appropriate values for these parameters, such as by using a heuristic like the elbow method.
2. Select an arbitary unvisited data point and mark it as visited
3. Gather all data points within distance $\epsilon$ to the selected. Common choices for the distance metric include Euclidean distances and Manhattan distances.
4. Calculate the number of data points gathered,

   4a. If the number of data points gathered is $\ge N$, form a new cluster and add the selected point and its neighbors to the cluster
    
   4b. Otherwise, mark the selected point as noise. Typically, this means adding the point to a separate cluster of noise points, rather than simply discarding it.
    
5. For each neighbor:

   5a. If the neighbor has not been visited, mark it as visited and gather all data points within distance $\epsilon$ to it.
   
   5b. If the number of neighbors gathered is $\ge N$, add these neighbors to the cluster as well. Specifically, the new neighbors should be added to the existing cluster, rather than forming a new cluster.
      
6. Repeat 4-5 until all points in the cluster have been seen.
7. Go back to step 2. Terminate when all points have been visited.



## Advantages/Disadvantages

✓ Unlike k-means clustering, the number of clusters in the data does not need to be specified beforehand.

✓ Can handle complex, non-linearly separable clusters, which makes it more robust to noise and outliers compared to other clustering algorithms like k-means.

✓ Computationally efficient for large datasets, as it only pairwise distances between nearby points need to be calculated, rather than all pairs of points.

✓ Can handle clusters of different shapes and sizes, unlike k-means, which assumes that all clusters are spherical and equally sized.

✗ Affected by the curse of dimensionality

✗ Clustering results are greatly affected by the choice of the distance metric and the parameters $\epsilon$ and $N$, so trial-and-error may be necessary 

✗ May not perform well on datasets with varying densities, as it relies on a fixed density threshold to determine cluster membership

## Implementation on Dataset

The DBSCAN algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/unsupervised-learning/dbscan/dbscan.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features for this classification task can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).

Since DBSCAN is an unsupervised learning method, the species labels are ignored. However, since I have them, I might as well use them to my advantage to understand how DBSCAN clusters the data, accounting for noise.
