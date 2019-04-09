# Coursera_Capstone

This is part of the IBM Applied Data Science Capstone project.


problem:  
finding a new location (location with 30,000 sqft) that our client can put a new location for their new (gym, indoor playyard, trampoline park.) The key is finding a location that is similar to the location that they have has success(60190)  

what impacts location?  

can we understand trafic flow  
housing  
income  
poverty   
distance to thinks of interest?    

Distance:Euclidean VS Haversine distance   


### Types of clustering algorithms  
  
#### Connectivity models: Data closer in space are catigorized as more similar(top-down | bottom-up)  
Distance function have an impact so which one should we use?   
> ##### Hierarchical Clustering([more info](https://stackabuse.com/hierarchical-clustering-with-python-and-scikit-learn/)
think about a dendrograms and how the data is seperated into groups  
>> Agglomerative:(bottom-up) Each observation starts in its own cluster, and pairs of clusters are merged as we move up the hierarchy.  
>> Divisive: (top-down) start with one cluster, then splits are performed recursively down the hierarchy.  

#### Centroid models: Data clusters is derived by the closeness of the data point to the centroid.   
Its is an iterative proccess of updating the centroids to find the local optima, so setting the seed could be important for reproducability. You need to define the number of clusters befor hand.   
>K-Means  
>>[youtube](https://www.youtube.com/watch?v=ZVhtchqHlHs)    
[youtube code](https://github.com/ardianumam/Machine-Learning-From-The-Scratch/blob/master/kernel_kMeansClustering.py)  
[other code](https://gist.github.com/mblondel/6230787)  

#### Distribution models: Data clusters based on probobalistic distributions
How probable is it that all data points in the cluster belong to the same distribution (Normal, Gaussian, ect). 
overfitting is a common problem.
Expectation-maximization algorithm(uses multivariate normal distributions)

#### Density Models:  
These models search the data space for areas of varied density of data points in the data space. It isolates various different density regions and assign the data points within these regions in the same cluster.
- Mean-Shift Clustering 
Every iteration the sliding window is shifted towards regions of higher density by shifting the center point to the mean of the points within the window. No need to select the number of cluster, the biggest drawback is the window size/radius “r” can be non-trivial
> <img src="https://cdn-images-1.medium.com/max/1000/1*bkFlVrrm4HACGfUzeBnErw.gif" width="250" height="250" />
- DBSCAN (Density-Based Spatial Clustering of Applications with Noise) 
> similar to mean-shift. You define the distance(ε-epsilon) that a point would be considered inside a neighborhood (All points which are within the ε distance are neighborhood points), as well as the "minPoints", which is the minimum number of point within the distance(ε) of the current point, otherwise the point is labeled as noise(which later become a cluster). 
> $Downside$: it doesn’t perform as well as others when the clusters are of varying density
> <img src="https://cdn-images-1.medium.com/max/1000/1*tc8UF-h0nQqUfLC8-0uInQ.gif" width="250" height="250" />
- OPTICS.  

