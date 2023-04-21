# DBSCAN: Density-Based Spatial Clustering of Applications With Noise

According to Wikipedia, DBSCAN "is a density-based clustering non-parametric algorithm: given a set of points in some space, it groups together points that are closely packed together (points with many nearby neighbors), marking as outliers points that lie alone in low-density regions (whose nearest neighbors are too far away)."

DBSCAN was first proposed in 1996 by Martin Ester, Hans-Peter Kriegel, Jörg Sander, and Xiaowei Xu.

## Algorithm

1. Choose $\epsilon>0$ and $N \ge 1$
2. Select an arbitary unvisited data point and mark it as visited
3. Gather all data points within distance $\epsilon$ to the selected
4. Calculate the number of data points gathered,

   4a. If the number of data points gathered is $\ge N$, form a new cluster and add the selected point and its neighbors to the cluster
    
   4b. Otherwise, mark the selected point as noise.
    
5. For each neighbor:

   5a. If the neighbor has not been visited, mark it as visited and gather all data points within distance $\epsilon$ to it.
   
   5b. If the number of neighbors gathered is $\ge N$, add these neighbors to the cluster as well.
      
6. Repeat 4-5 until all points in the cluster have been seen.
7. Go back to step 2. Terminate when all points have been visited.

## Advantages/Disadvantages

✓ Unlike k-means clustering, the number of clusters in the data does not need to be specified beforehand.
<br></br>
✗ Affected by the curse of dimensionality

## Implementation on Dataset
