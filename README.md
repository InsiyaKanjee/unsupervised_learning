# Cryptocurrency Clusters

### Data Preparation

* Read `crypto_data.csv` into Pandas. The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

* Discarded all cryptocurrencies that are not being traded. In other words, filtered for currencies that are currently being traded. Dropped the `IsTrading` column from the dataframe.

* Removed all rows that have at least one null value.

* Filtered for cryptocurrencies that have been mined. That is, the total coins mined should be greater than zero.

* Deleted the `CoinName` from the original dataframe

* Standardized the dataset so that columns that contain larger values do not unduly influence the outcome.

### Dimensionality Reduction

* Creating dummy variables above dramatically increased the number of features in the dataset. Performed dimensionality reduction with PCA. Rather than specify the number of principal components, stated the desired **explained variance** of 0.90.

* Next, further reduced the dataset dimensions with t-SNE and visually inspect the results. In order to accomplish this task, ran t-SNE on the principal components: the output of the PCA transformation. Then created a scatter plot of the t-SNE output.

### Cluster Analysis with k-Means

* Created an elbow plot to identify the best number of clusters. Used a for-loop to determine the inertia for each `k` between 1 through 10. 

### Recommendation

* Based on your findings, made a brief recommendation.

