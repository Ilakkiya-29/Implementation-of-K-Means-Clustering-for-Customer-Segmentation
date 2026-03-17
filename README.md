# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries such as pandas, matplotlib, and KMeans from sklearn.
2. Load the dataset Mall_Customers.csv using pandas and select the features Annual Income and Spending Score.
3. Apply the K-Means clustering algorithm with a chosen number of clusters (k = 5).
4. Fit the model to the data and predict the cluster for each customer.
5. Add the predicted cluster values to the dataset.
6. Visualize the clusters using a scatter plot and mark the centroids of each cluster.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Ilakkiya K
RegisterNumber: 212225040130
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("Mall_Customers.csv")
X = data[['Annual Income (k$)', 'Spending Score (1-100)']]
print(data.head())
kmeans = KMeans(n_clusters=5, random_state=42)
y_kmeans = kmeans.fit_predict(X)


data['Cluster'] = y_kmeans

print("\nClustered Data:")
print(data.head())


plt.figure()
plt.scatter(X[y_kmeans == 0]['Annual Income (k$)'], 
            X[y_kmeans == 0]['Spending Score (1-100)'], label='Cluster 0')

plt.scatter(X[y_kmeans == 1]['Annual Income (k$)'], 
            X[y_kmeans == 1]['Spending Score (1-100)'], label='Cluster 1')

plt.scatter(X[y_kmeans == 2]['Annual Income (k$)'], 
            X[y_kmeans == 2]['Spending Score (1-100)'], label='Cluster 2')

plt.scatter(X[y_kmeans == 3]['Annual Income (k$)'], 
            X[y_kmeans == 3]['Spending Score (1-100)'], label='Cluster 3')

plt.scatter(X[y_kmeans == 4]['Annual Income (k$)'], 
            X[y_kmeans == 4]['Spending Score (1-100)'], label='Cluster 4')

# Plot centroids
plt.scatter(kmeans.cluster_centers_[:,0], 
            kmeans.cluster_centers_[:,1], 
            s=200, label='Centroids')

plt.title("Customer Segmentation using K-Means")
plt.xlabel("Annual Income (k$)")
plt.ylabel("Spending Score (1-100)")
plt.legend()
plt.show()
*/
```

## Output:
<img width="666" height="713" alt="image" src="https://github.com/user-attachments/assets/2da766fc-3a4b-49af-a3b3-d18ff237cd21" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
