# CryptoClustering
Applying unsupervised learning techniques to determine the optimal k-value, normalizing the data, and visualizing the resulting clusters using a scatter plot. Subsequently, comparing these results with those obtained after applying Principal Component Analysis (PCA).

## Technologies and Tools Used
- Python
- Jupyter Lab
- scikit-learn 
- pandas
- hvplot

## Instructions
I followed below steps to use K-means algorithm to make predictions and compare the results after applying PCA (Principal Component Analysis)

### 1. Prepare data
Used StandardScaler() to normalize data from the CSV file


### 2. Find the Best Value for k Using the Scaled DataFrame
Plotted a line chart with all the inertia values computed with the different k values to indentify the optimal value


### 3. Cluster Cryptocurrencies with K-means Using the Scaled DataFrame
The optimal k value was 4. Created a scatter plot using hvPlot


### 4. Optimize Clusters with Principal Component Analysis (PCA)
Used original scaled DataFrame and performed a PCA with 3 principal components. Based on explained variance ratio, about 89% of the total variance is condensed into the 3 PCA variables. 
<br> array([0.3719856 , 0.34700813, 0.17603793])

### 5. Find the Best Value for k Using the PCA DataFrame
Used the elbow method on the scaled PCA DataFrame to find the best k-value as 4.


###  6. Create Composite Plots to compare the Plots for the Analysis
Our analysis showed that optimal k-value before and after PCA was 4.

- On the PCA-reduced data, clusters appear tighter. PCA effectively captured the most significant variance in the data while filtering out noise and irrelevant features. With fewer dimensions, K-Means formed more compact and well-separated clusters. Although some outliers remain in the graph, the overall clustering is noticeably improved compared to the original data before PCA optimization.

- Examining the inertia values further supports this improvement. Before PCA, inertia starts at 287 and decreases as the number of clusters increases. After PCA, the initial inertia is already lower at 256.87 and continues to drop. This indicates that PCA successfully reduced noise and redundant dimensions, leading to more compact clusters. The reduction in inertia is particularly significant for lower k-values, suggesting that PCA enhanced the natural grouping of the data and improved cluster definition.

## References
- ASU Bootcamp Class Activities
- chatGPT
Composite plots
