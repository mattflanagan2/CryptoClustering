# CryptoClustering
## Background
In this challenge, you’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.
This repository contains code for clustering cryptocurrencies using K-means clustering. The analysis is performed using both the original scaled data and the Principal Component Analysis (PCA) reduced data.


## Steps
### Import the Data
The data is imported from the CSV file and displayed as a pandas dataframe.

<img width="1327" alt="Screenshot 2024-04-15 at 11 14 46 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/11f1168d-99e7-4dd3-8e0f-472dc67690ce">


### Prepare the Data
The data from the CSV file is normalized using the `StandardScaler()` module from scikit-learn. A DataFrame with the scaled data is created, and the "coin_id" index from the original DataFrame is set as the index for the new DataFrame.

<img width="1328" alt="Screenshot 2024-04-15 at 11 15 32 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/98dab6b3-ac4d-42a7-93a9-bcfd1f88b0a9">
<img width="1328" alt="Screenshot 2024-04-15 at 11 15 42 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/223c8e19-3861-4e61-8985-b32bd2edad17">
<img width="1309" alt="Screenshot 2024-04-15 at 11 15 58 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/3e817820-065a-4a89-86ff-00e8a413f233">

### Finding the Best Value for k
The elbow method is employed to find the optimal value for k. A line chart is plotted with inertia values computed for different values of k. According to the elbow curve, the best value for k is 4.

<img width="1317" alt="Screenshot 2024-04-15 at 11 17 18 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/9880a655-b7b9-47fa-817e-5743897863d6">
<img width="1317" alt="Screenshot 2024-04-15 at 11 17 28 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/03efa7cb-955c-432e-b4d2-a0affca3b380">
<img width="1317" alt="Screenshot 2024-04-15 at 11 17 44 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/821844f2-66b9-4e6c-b892-4f1c41b68108">

### Clustering Cryptocurrencies with K-means
Cryptocurrencies are clustered using K-means clustering with the best value for k obtained from the previous step. A scatter plot is created to visualize the clusters, with data points colored according to their respective clusters.

<img width="1317" alt="Screenshot 2024-04-15 at 11 19 49 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/d9f575d1-73cd-46aa-8cb3-5390f200f246">
<img width="1317" alt="Screenshot 2024-04-15 at 11 20 05 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/a47b8f2c-5ba4-49cb-b285-8ddbb0bb2155">
<img width="1317" alt="Screenshot 2024-04-15 at 11 20 17 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/eb839917-963a-4fb8-a95d-ed67834182dc">
<img width="1317" alt="Screenshot 2024-04-15 at 11 20 29 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/248ed78f-0cbd-472f-bd53-356001e32e9f">
<img width="843" alt="Screenshot 2024-04-15 at 11 20 47 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/22ce85d5-266d-480c-a698-47f24983050c">

### Optimizing Clusters with Principal Component Analysis
Principal Component Analysis is performed on the original scaled DataFrame to reduce the features to three principal components. The explained variance is retrieved to determine the information attributed to each principal component.

<img width="1277" alt="Screenshot 2024-04-15 at 11 23 22 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/be9c3274-da7c-4a79-a718-3a80894177c2">
<img width="1277" alt="Screenshot 2024-04-15 at 11 23 56 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/6f547da2-0a44-4c23-8d8c-0d1ea6de10e2">

According to the PCA, the explained variance ratio is 89.5%

### Finding the Best Value for k Using PCA Data
Similar to the previous step, the elbow method is applied to the PCA data to find the optimal value for k.
Again, according to the elbow curve the best value for k is 3-4, for my analysis I used 4.

<img width="1277" alt="Screenshot 2024-04-15 at 11 32 53 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/528764ab-34f7-4a0d-8ac3-0dac954bf849">
<img width="1277" alt="Screenshot 2024-04-15 at 11 33 08 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/0d88349f-3c89-4b9a-bc08-a1eb067dd805">
<img width="842" alt="Screenshot 2024-04-15 at 11 33 45 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/158a550d-d8d6-43a9-ba98-a224cbef17ee">

### Clustering Cryptocurrencies with K-means Using PCA Data
Cryptocurrencies are clustered using K-means with the best value for k obtained from the PCA data. A scatter plot is created to visualize the clusters, this time using fewer features.

<img width="1318" alt="Screenshot 2024-04-15 at 11 35 10 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/2d65656a-a4fe-4dab-924b-4569e1d7dee2">
<img width="1318" alt="Screenshot 2024-04-15 at 11 35 21 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/d8b9a06b-7f90-4664-8dca-cce0ea031e55">
<img width="1318" alt="Screenshot 2024-04-15 at 11 35 32 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/e8f65a17-39e8-4f92-99df-580cd92f995d">
<img width="1318" alt="Screenshot 2024-04-15 at 11 36 19 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/b4286f35-a914-45b7-b3b9-29f174e34229">
<img width="841" alt="Screenshot 2024-04-15 at 11 36 36 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/95b1d625-17b2-4e97-9503-a9eb4543a83a">

### Visualizing and Comparing Results
The impact of using fewer features for clustering is discussed, comparing the results obtained from the original scaled data and the PCA data.

<img width="1324" alt="Screenshot 2024-04-15 at 11 38 59 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/3a4489df-e269-4783-8799-2679be769ebd">
<img width="1324" alt="Screenshot 2024-04-15 at 11 39 13 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/68fbbdf7-154a-4b39-a12f-0be9c39254a4">
<img width="838" alt="Screenshot 2024-04-15 at 11 39 31 AM" src="https://github.com/mattflanagan2/CryptoClustering/assets/146908072/a429bc2d-71cf-4e6f-8152-a6c36df26349">

To increase the readability of the scatter plot, the original data points are plotted as circles adn the PCA data points are plotted as squares.

The following question was then answered.  

**Question:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

**Answer:** 
  Reducing the number of features used for clustering with K-Means results in decreased differentiation between clusters. By opting for a smaller number of clusters, more data points are forced to fit within each cluster, potentially leading to a loss of granularity in the clustering. For instance, choosing 3 clusters over 4 means that the data is condensed into fewer groups, possibly overlooking distinct patterns or characteristics present in the dataset. This reduction in dimensionality may simplify the analysis but could also obscure valuable insights and nuances within the data.

For detailed implementation and analysis, please refer to the Jupyter notebook in this repository.
