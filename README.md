# Crypto Clustering

This project aims to cluster cryptocurrencies based on their price change data using the K-Means algorithm and Principal Component Analysis (PCA). The analysis helps identify patterns and similarities among different cryptocurrencies, which can be useful for investment strategies or understanding market trends.

## Data

The project uses a CSV file named `crypto_market_data.csv` containing price change percentage data for various cryptocurrencies over different time periods (24 hours, 7 days, 14 days, 30 days, 60 days, 200 days, and 1 year).

## Analysis

The analysis is performed in the following steps:

1. **Import the Data**: The CSV file is imported into a Pandas DataFrame, and summary statistics are generated to understand the data.
2. **Prepare the Data**: The data is scaled using the `StandardScaler` from scikit-learn to normalize the features.
3. **Find the Best Value for k (Original Data)**: The elbow method is used to determine the optimal number of clusters (k) for the original data. A line chart is plotted to visualize the inertia values for different values of k.
4. **Cluster Cryptocurrencies with K-Means (Original Data)**: The K-Means algorithm is applied to the original data using the optimal value of k found in the previous step. The resulting clusters are added to the DataFrame, and a scatter plot is created to visualize the clusters.
5. **Optimize Clusters with Principal Component Analysis (PCA)**: PCA is performed to reduce the dimensionality of the data to three principal components. The explained variance is calculated to determine the information captured by the principal components.
6. **Find the Best Value for k (PCA Data)**: The elbow method is used again to find the optimal value of k for the PCA data.
7. **Cluster Cryptocurrencies with K-Means (PCA Data)**: The K-Means algorithm is applied to the PCA data using the optimal value of k found in the previous step. The resulting clusters are added to the DataFrame, and a scatter plot is created to visualize the clusters.
8. **Visualize and Compare the Results**: Composite plots are created to contrast the elbow curves and cluster visualizations for the original and PCA data. The impact of using fewer features (PCA data) for clustering is analyzed.

## Dependencies

The project requires the following Python libraries:

- pandas
- scikit-learn
- hvplot (holoviews)