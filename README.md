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
![alt text](images/b1.jpg)
![alt text](images/gender.jpg)
![alt text](images/b2.jpg)
![alt text](images/culmen_length_mm.jpg)
![alt text](images/culmen_depth_mm.jpg)
![alt text](images/flipper_length_mm.jpg)
![alt text](images/body_mass_g.jpg)

# 3. Principal Component Analysis (PCA)
![alt text](images/c1.jpg)
![alt text](images/c2.jpg)

# 4. K-Means Clustering
![alt text](images/d1.jpg)
![alt text](images/Change_in_Inertia.jpg)
![alt text](images/Interia_Trend.jpg)
![alt text](images/d2.jpg)
![alt text](images/3d_kmean.jpg)
![alt text](images/d3.jpg)
![alt text](images/2_vs_3_PCproj.jpg)
![alt text](images/3_vs_1_PCproj.jpg)
![alt text](images/1_vs_2_PCproj.jpg)

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
