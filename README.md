## CryptoClustering using K-Means

This repository contains code for clustering cryptocurrencies based on their market performance data. The data includes various price change percentages for different holding periods. The primary goal is to group cryptocurrencies with similar price trends and behaviors into clusters.

### Data Preparation and Exploration

The provided Python code demonstrates the following steps:
1. Import necessary libraries and dependencies, such as pandas, scikit-learn, matplotlib, and Holoviews.
2. Load the cryptocurrency market data from a CSV file into a Pandas DataFrame (`df_market_data`).
3. Display a sample of the loaded data.
4. Generate summary statistics for the data, including mean, standard deviation, minimum, maximum, etc.
5. Plot a line chart using the `hvplot` library to visualize the price change percentages for different cryptocurrencies over different holding periods.

### Data Preprocessing

1. Use the `StandardScaler()` module from scikit-learn to normalize the data in `df_market_data`.
2. Create a new DataFrame (`df_market_data_scaled`) with the scaled data.
3. Copy the cryptocurrency names from the original data to the scaled data.
4. Set the cryptocurrency names as the index of the scaled data.

### Finding the Optimal Number of Clusters (k)

1. Calculate the inertia values (sum of squared distances from each point to its assigned center) for different values of k (number of clusters) using the original scaled data.
2. Create an elbow curve plot to visualize the inertia values for different k values and identify the optimal value for k. In this case, the elbow point in the curve helps determine the optimal number of clusters.

### Clustering Cryptocurrencies using K-Means

1. Initialize the K-Means model with the optimal number of clusters obtained from the elbow curve analysis.
2. Fit the K-Means model to the scaled data and predict the clusters for each cryptocurrency.
3. Assign the cluster labels to the original data for further analysis and visualization.

### Principal Component Analysis (PCA)

1. Perform Principal Component Analysis (PCA) on the scaled data to reduce the dimensionality while retaining as much information as possible.
2. Calculate the explained variance ratios of the principal components to understand how much variability each component explains.
3. Create a new DataFrame (`df_market_data_pca`) with the first three principal components and cryptocurrency names.

### Finding the Optimal Number of Clusters with PCA Data

1. Calculate the inertia values for different values of k using the principal components obtained from PCA.
2. Create an elbow curve plot to visualize the inertia values for different k values and determine the optimal number of clusters.

### Clustering Cryptocurrencies with PCA Data

1. Initialize the K-Means model using the optimal number of clusters obtained from PCA analysis.
2. Fit the K-Means model to the PCA-transformed data and predict the clusters for each cryptocurrency.
3. Assign the cluster labels to the original data with PCA principal components for further analysis.

This code repository aims to provide insights into clustering cryptocurrencies based on market performance data. It demonstrates how to preprocess the data, find the optimal number of clusters, and perform clustering using both original and PCA-transformed data.

