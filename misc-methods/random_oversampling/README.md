# Random Oversampling & Random Undersampling

Random oversampling and random undersampling are techniques used in machine learning to address class imbalance in a dataset. Class imbalance occurs when one class (the minority class) is underrepresented in the dataset compared to the other class(es) (the majority class). In this situation, a machine learning model may become biased towards the majority class, resulting in poor performance when predicting the minority class. 

## Random Oversampling

Random oversampling is a technique used to address class imbalance by **increasing the number of instances in the minority class.** This is achieved by randomly duplicating samples from the minority class until it is balanced with the majority class. Random oversampling is a simple and effective technique that can improve the performance of a model when dealing with imbalanced datasets. However, it may lead to overfitting and may not work well when the minority class is very small.

### Advantages/Disadvantages

✓ Simple and effective in improving performance for imbalanced datasets

✓ Preserves the original data and does not discard any information

✗ May lead to overfitting and reduced generalization to new data

✗ May not work well when the minority class is very small

## Random Undersampling

Random undersampling is a technique used to address class imbalance by **reducing the number of instances in the majority class.** This is achieved by randomly selecting a subset of samples from the majority class until it is balanced with the minority class. Random undersampling is a simple and fast technique, but it may result in loss of important information if important samples are discarded. Furthermore, if the minority class is very small, random undersampling may not be effective.

### Advantages/Disadvantages

✓ Simple and fast technique for addressing class imbalance

✓ Can be effective in balancing the dataset

✗ May result in loss of important information if important samples are discarded

✗ May not work well when the minority class is very small

## Implementation on Dataset

Random oversampling and random undersampling are implemented in [this Jupyter notebook](https://github.com/kary5678/INDE-577/blob/main/misc-methods/random_oversampling/random_oversampling.ipynb) using the [Hawks](https://github.com/kary5678/INDE-577/blob/main/Data/hawks.csv) dataset. This data contains observations for 3 species of hawks (which will formulate the binary classes) and features such as age, sex, wing length, body weight, tail length, etc. More details about this dataset and visualizations of the relevant features can be found in the [hawks analysis notebook](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb).
