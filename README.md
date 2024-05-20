# Penguins_Unsupervised_Classification

This is a project that aims to group penguins with 3 unsupervised machine learning methods: K-Means Clustering, Hierarchical Clustering and  Density-Based Spatial Clustering of Applications with Noise (DBSCAN). The dataset, can be found in the current directory in .csv format.

The project is presented in the following structure:

**1. Data Access and Processing**

**2. Data Visualization**
   
**3. Principal Component Analysis (PCA)**
   
**4. K-Means Clustering**   

**5. Hierarchical Clustering**   

**6. Density-Based Spatial Clustering of Applications with Noise (DBSCAN)**




Let's do this.
*****************************************************************************************************************
# 1. Data Access and Processing

Let's look at the original dataset, there are 5 variables, which are their biological features:
![alt text](images/a1.jpg)

First step to clean the dataset is to see if there is any outliner(s). Through the statistics info, the minimum and maximum flipper length do not make sense, while one is negative and the other one is much higher than the mean. On the other hand, the numerical variables seems fine.

![alt text](images/a2.jpg)

This is more obvious in a boxplot:
![alt text](images/boxplot.jpg)

Two conditional statements would take care of the outliners:
![alt text](images/a3.jpg)

Now for the gender column, conditional statement for taking out instance that the gender of penguin is not male and female. We see that one more instance is taken out. Now, the dataset is ready:
![alt text](images/a4.jpg)

Next step is to split the gender column into male and female column:
![alt text](images/a5.jpg)

And change the columns into binary integer, now let's see the statistics info:
![alt text](images/a6.jpg)

# 2. Data Visualization

A simple pie chart can help us understand the gender situation in the dataset:
![alt text](images/b1.jpg)
![alt text](images/gender.jpg)

As per the continuous variables, a for-loop is used to see the distributions of each variable:
![alt text](images/b2.jpg)

How long are the culmens?
![alt text](images/culmen_length_mm.jpg)

How deep are the culmens?
![alt text](images/culmen_depth_mm.jpg)

How about the flippers?
![alt text](images/flipper_length_mm.jpg)

The birds' body mass?
![alt text](images/body_mass_g.jpg)

# 3. Principal Component Analysis (PCA)

In this project, although this is not a large dataset, but it is still worth to use PCA to reduce the dimensionality of the dataset and hence the computation cost and time. It is done by transforming the dataset linearly into a new coordinate system, while the axes of the system are called "principal component". To reduce the dimensionality, only several axes are kept such that maximize the variance (set by the user) explained by the data.

To simplify the calculation, all variables are scaled with the standard normal distribution:
![alt text](images/c1.jpg)

After the transformation, the data was fitted and the 3 principal components were chosen so that 95% of the variance can be explained by the data:
![alt text](images/c2.jpg)

With the transformed data and 3 axes only, now we can move to the unspervised methods.

# 4. K-Means Clustering

K-Means Clustering is the first method used. A set of number, from k=1 to k=9, is set to be the number of clusters and see which number is the best, with the use of the Elbow method.

For each k, random k points are selected in the dataset, for calculating the mean Euclidean distance and variance (or inertia, if preferred) for each selected point. Note that the k points which give the lowest total variance are selected for each k.

![alt text](images/d1.jpg)

To select the reasonable k, as mentioned, Elbow method is used. The plot for the change in lowest variance, from k to k+1 is shown. It is obvious that from k=5 to k=6, the change in variance is still large while the change is low from k=6 to k=7:

![alt text](images/Change_in_Inertia.jpg)

This can also be visualized by just plotting the lowest variance for each k. The variance keeps almost the same after k=6. As a result, we use k=6 as the number of cluster.

![alt text](images/Interia_Trend.jpg)

Now it is the time to see the result, by performing k-means method with k=6 and the tranformed dataset. All data are now classified and can be shown in a 3d scatter plot with 3 principal components chosen:

![alt text](images/d2.jpg)
![alt text](images/3d_kmean.jpg)

The result can be understand in a better way: using projection of the above 3d scatter plots. Three 2d scatter plots with different combination of principal components ( $2^{nd}$ vs $3^{rd}$, $3^{rd}$ vs $1^{st}$ and $1^{st}$ vs $2^{nd}$ ) are shown below.

![alt text](images/d3.jpg)
![alt text](images/2_vs_3_PCproj.jpg)
![alt text](images/3_vs_1_PCproj.jpg)
![alt text](images/1_vs_2_PCproj.jpg)

It is obvious that each cluster is separated from others in at least one of the principal component combination. If one of the cluster cannot be separated from others in all combination, wrong k is chosen (may be those overlapping clusters are indeed one group!). The result shows k-means clustering method works well when k=6 is used.

# 5. Hierarchical Clustering
![alt text](images/e1.jpg)
![alt text](images/den.jpg)
![alt text](images/e2.jpg)
![alt text](images/e3.jpg)
![alt text](images/hc.jpg)

# 6. Density-Based Spatial Clustering of Applications with Noise (DBSCAN)
![alt text](images/f1.jpg)
![alt text](images/f2.jpg)
![alt text](images/N_clusters_DBSCAN.jpg)
![alt text](images/Sil_score_DBSCAN.jpg)
![alt text](images/f3.jpg)
![alt text](images/f4.jpg)
![alt text](images/f5.jpg)
![alt text](images/f6.jpg)
![alt text](images/DBSCAN.jpg)
