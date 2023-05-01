# Feature Selection

Feature selection is the process of selecting a subset of the original features in a dataset to use in a machine learning model. The goal of feature selection is to improve model performance by reducing the number of irrelevant, redundant, or noisy features in the data. It is an important step in preparing data for machine learning as it reduces dimensionality/complexity and increases interpretability, while also making the model more efficient and easier to work with. By choosing the appropriate feature selection method and carefully evaluating the performance of the model, one can create more effective and accurate machine learning models.

## Popular Techniques

There are several popular techniques for feature selection, including:

1. **Filter methods**: selecting features based on statistical measures such as correlation, mutual information, or chi-squared tests

2. **Wrapper methods**: selecting features based on how well they perform on a specific machine learning algorithm

3. **Embedded methods**: selecting features as part of the training process of a machine learning algorithm

4. **Dimensionality reduction techniques**: using PCA or t-SNE to reduce the number of features in a dataset

5. **Tree-based methods**: random forests or decision trees can be used for feature selection by measuring the importance of each feature in the algorithm

Then, evaluate performance of the model using the selected features, and iterate and refine the feature selection process as needed.

## Advantages/Disadvantages

✓ Improved model performance by removing irrelevant or redundant features from the dataset, leading to higher accuracy and lower error rates

✓ Reduced complexity by selecting only the most informative features, simplifying models and making them easier to implement and maintain

✓ Increased interpretability by reducing the number of features and making it easier to understand how the model is making its predictions

✓ Reduced risk of overfitting

✗ Information loss if features that are marginally relevant are removed.

✗ Increased bias if the selected features do not adequately represent the underlying distribution of the data

✗ Poor generalization to new data if done poorly or without proper validation

✗ Can be computationally expensive, especially for large datasets or complex models

## Implementation on Dataset

Feature selection is implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/misc-methods/feature_selection/feature_selection.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
