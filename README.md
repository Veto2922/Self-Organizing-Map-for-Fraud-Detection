# Self Organizing Map for Fraud Detection

## Overview
This notebook demonstrates the implementation of a Self-Organizing Map (SOM) for detecting fraud in credit card applications. The SOM is trained on a dataset of credit card applications to learn patterns and identify potential outliers that may indicate fraudulent activities.

## Setup and Dependencies
To run this notebook, you need to install the `MiniSom` package using pip:
```bash
pip install MiniSom
```

Additionally, the following libraries are imported within the notebook:
- `numpy` (as `np`) for numerical operations
- `pandas` (as `pd`) for data manipulation
- `matplotlib.pyplot` (as `plt`) for data visualization
- `MinMaxScaler` from `sklearn.preprocessing` for feature scaling
- `MiniSom` from `minisom` for implementing the Self-Organizing Map

## Dataset
The dataset used in this notebook is `Credit_Card_Applications.csv`, which contains information about credit card applications. It includes various features describing the applicants and whether their applications were approved or rejected.

## Implementation
1. **Data Preprocessing**: The dataset is loaded and preprocessed. Features and target values are separated, and feature scaling is applied using `MinMaxScaler` to scale all feature values between 0 and 1.

2. **Training the SOM**: A Self-Organizing Map (SOM) is initialized using the `MiniSom` class with parameters such as grid dimensions (`x` and `y`), input dimensionality (`input_len`), spread of the neighborhood function (`sigma`), and learning rate (`learning_rate`). The SOM is then trained using the `train_random` method for a specified number of iterations.

3. **Visualization**: The SOM is visualized to observe the distribution of data points in the SOM grid. Additionally, markers are plotted on the grid to indicate the presence of potential outliers, which are considered as fraud candidates.

4. **Identifying Fraudulent Cases**: Finally, the SOM is used to identify potential frauds by locating outliers on the grid. The fraud cases are extracted and transformed back to their original scale using inverse feature scaling.

## Conclusion
The SOM provides a visual representation of the credit card application data, facilitating the identification of potential frauds based on their proximity to outliers in the SOM grid. This approach offers a useful technique for fraud detection in applications where traditional methods may fall short.
