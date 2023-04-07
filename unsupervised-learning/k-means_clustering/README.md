# *k*-Means Clustering

## Algorithm

0. Normalize/scale the data appropriately
1. Choose $k \ge 1$
2. Place k centroids on the feature space
3. Assign each data point to a centroid, specifically the nearest one
4. Update the centroids by assigning them to the average of all the points in the respective cluster
5. Repeat steps 3-4 until the clusters stop moving