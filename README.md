# CryptoClustering

# Introduction
In this challenge, you'll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

# Requirements
Find the Best Value for k by Using the Scaled DataFrame (15 points)
To receive all points, you must:
Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11. (5 points)
To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k. (5 points)
Answer the following question: What's the best value for k? (5 points)

Cluster the Cryptocurrencies with K-Means by Using the Scaled DataFrame (10 points)
To receive all points, you must:
Initialize the K-means model with best value for k. (1 point)
Fit the K-means model by using the scaled DataFrame. (1 point)
Predict the clusters for grouping the cryptocurrencies by using the scaled DataFrame. Review the resulting array of cluster values. (3 points)
Create a copy of the scaled DataFrame, and then add a new column of the predicted clusters. (1 point)
Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Color the graph points with the labels that you found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents. (4 points)

Optimize the Clusters with Principal Component Analysis (10 points)
To receive all points, you must:
Create a PCA model instance, and set n_components=3. (1 point)
Use the PCA model to reduce the features to three principal components. (2 points)
Get the explained variance to determine how much information can be attributed to each principal component. (2 points)
Answer the following question: What's the total explained variance of the three principal components? (3 points)
Create a new DataFrame from the scaled PCA data. Be sure to set the coin_id index from the original scaled DataFrame as the index for the new DataFrame. Review the first five rows of the DataFrame. (2 points)

Find the Best Value for k by Using the PCA DataFrame (10 points)
To receive all points, you must:
Code the elbow method algorithm, and use the scaled PCA DataFrame to find the best value for k. Use a range from 1 to 11. (2 points)
To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k. (5 points)
Answer the following questions: What's the best value for k when using the scaled PCA DataFrame? Does it differ from the best value for k that you found by using the original scaled DataFrame? (3 points)

Cluster the Cryptocurrencies with K-means by Using the PCA DataFrame (10 points)
To receive all points, you must:
Initialize the K-means model with the best value for k. (1 point)
Fit the K-means model by using the PCA data. (1 point)
Predict the clusters for grouping the cryptocurrencies by using the PCA data. Review the resulting array of cluster values. (3 points)
Create a copy of the scaled PCA DataFrame, and then add a new column of the predicted clusters. (1 point)
Using hvPlot, create a scatter plot by setting x="PC1" and y="PC2". Color the graph points with the labels that you found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents. (4 points)

Visualize and Compare the Results (15 points)
To receive all points, you must:
Create a composite plot by using hvPlot and the plus sign (+) operator to compare the elbow curve that you created from the original scaled DataFrame with the one that you created from the scaled PCA DataFrame. (5 points)
Create a composite plot by using hvPlot and the plus (+) operator to compare the cryptocurrency clusters that resulted from using the original scaled DataFrame with those that resulted from the scaled PCA DataFrame. (5 points)
Answer the following question: Based on visually analyzing the cluster analysis results, what's the impact of using fewer features to cluster the data by using K-means? (5 points)

Coding Conventions and Formatting (10 points)
To receive all points, you must:
Place imports at the top of the file, just after any module comments and docstrings, and before module globals and constants. (3 points)
Name functions and variables with lowercase characters, with words separated by underscores. (2 points)
Follow DRY (Don't Repeat Yourself) principles, creating maintainable and reusable code. (3 points)
Use concise logic and creative engineering where possible. (2 points)

Deployment and Submission (10 points)
To receive all points, you must:
Submit a link to a GitHub repository that's cloned to your local machine and that contains your files. (4 points)
Use the command line to add your files to the repository. (3 points)
Include appropriate commit messages in your files. (3 points)

Code Comments (10 points)
To receive all points, your code must:
Be well commented with concise, relevant notes that other developers can understand. (10 points)

# Analysis
![Scaled Elbow Curve](https://github.com/user-attachments/assets/6fdb46a6-a577-4e3f-b3df-73e7627fd957)


![PCA Elbow Curve](https://github.com/user-attachments/assets/88b87cc0-5d30-4b17-ba13-e457f0cac285)

  Eblow Curve Comparisons: 
  Both elbow curves show the same ideal K value of 4, but the elbow curve for the PCA data shows a lower inertia value of 49 compared to 79. 

  The scaled original data uses scaling to standardize the data (ie mean=0, standard deviation= 1) and makes the influence of all features equal. The higher inertia indicates that the data has more dispersed clusters. 

  The PCA data reduces the features by focusing only on the most important pieces that explain the variance. The lower inertia would indicate that the clusters are closer and more compact. This is due to PCA filtering out less significant variance and reducing the noise.

![Scaled Hover Plot](https://github.com/user-attachments/assets/e542d73e-684d-43dc-b43e-85e3824fda71)

![PCA Hover Plot](https://github.com/user-attachments/assets/e009692f-90fa-49ba-a738-9bc9b5380c5f)


  Scatter Cluster Comparisons:

  The first cluster graph (scaled original data) shows that the clusters are overlapping and it is difficult to see distinct clusters. This would indicate that more features being used may not be the best option since there are no clear underlying patterns or structure to the clusters.

  The second cluster graph (PCA data) shows that the clusters do not overlap as much. There are much more defined clusters- all 4 are clearly visible. This would indicate that using less features reduced the noice and gives insight to patterns in the data. 

