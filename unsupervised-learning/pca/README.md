# PCA: Principal Component Analysis

Invented in 1901 by Karl Pearson as an analogue of the principal axis theorem in mechanics, principal component analysis (abbreviated as PCA) aims to find a lower-dimensional representation of the data that captures the most important patterns in the original data. This dimensionality reduction method is an unsupervised learning method that can transform a large set of variables into a smaller one that still contains most of the information in the large set.

PCA can be used for various purposes, such as reducing the dimensionality of the data, visualizing high-dimensional data, and denoising data. The algorithm is widely used in machine learning and data analysis for preprocessing and feature extraction.

## Algorithm

1. **Standardize (center and scale) the data.** PCA requires the data to be centered around the mean and scaled to have unit variance. Therefore, we first subtract the mean from each feature and divide by the standard deviation to get a standardized version of the data.

2. **Compute the covariance or correlation matrix.** The covariance matrix measures the linear relationship between pairs of features in the data. We compute the covariance matrix of the standardized data, which is an n x n matrix, where n is the number of features in the data.

3. **Find the eigenvectors and eigenvalues of the covariance matrix.** Eigenvectors are the directions in which the data varies the most, while eigenvalues represent the amount of variance explained by each eigenvector. Eigenvectors and eigenvalues of the covariance matrix can be computed using linear algebra. Then, sort the eigenvectors in decreasing order of eigenvalue, so that the eigenvectors with the highest variance (and therefore the most important) come first.

4. **Choose the number of principal components.** Tthe number of principal components to keep is chosen based on the desired amount of variance to be retained. This can be determined by looking at the explained variance ratio, which is the proportion of the total variance explained by each principal component.

5. **Reduce the dimension of the data.** Project the data onto the new feature space by taking the top k eigenvectors (where k is the chosen number of principal components) and use them to transform the data. This new feature space has k dimensions, where each dimension corresponds to a principal component.

## Useful Metrics To Know

* **Explained variance ratio.** This metric measures the proportion of the total variance in the data that is explained by each principal component. It can be used to determine the number of principal components to keep in order to retain a desired amount of variance.

* **Principal component loadings**. The principal component loadings are the weights assigned to each feature in each principal component. These loadings can be used to identify which features are most important in explaining the variation in the data.

## Advantages/Disadvantages
✓ Dimensionality reduction: PCA can be used to reduce the number of features in the data by projecting it onto a lower-dimensional space. This can help to simplify the analysis and visualization of high-dimensional data.

✓ Feature extraction: The principal components obtained from PCA can be used as new features in machine learning models, which may improve their performance compared to using the original features.

✓ Noise reduction: PCA can help to reduce the effects of noise and improve the signal-to-noise ratio in the data.

✓ Interpretability: The principal components obtained from PCA can be interpreted as linear combinations of the original features, which can help to identify which features are most important in explaining the variation in the data.
<br></br>
✗ Information loss: PCA can result in some loss of information when the data is projected onto a lower-dimensional space. The amount of information lost depends on the number of principal components retained.

✗ Assumes linearity: PCA assumes that the relationship between the features is linear. If the relationship is nonlinear, PCA may not be the most effective technique for dimensionality reduction.

✗ Sensitivity to outliers: PCA is sensitive to outliers in the data, which can affect the estimation of the covariance matrix and the principal components.

✗ Computationally intensive: PCA can be computationally intensive, especially for large datasets. This can make it challenging to apply to high-dimensional data in real-time applications.

## Implementation on Dataset

The PCA algorithm discussed above is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/unsupervised-learning/pca/pca.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features for this classification task can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).

Since PCA is an unsupervised learning method, the species labels are ignored. However, since I have them, I might as well use them to my advantage. Following implemntation of PCA, I fit a *k*-nearest neighbors model using the principal components, comparing the classification accuracy to the *k*-nearest neighbors model I had fit with the unreduced data.
