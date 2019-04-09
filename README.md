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
DBSCAN 
OPTICS.
Mean-Shift Clustering
> <img src="https://cdn-images-1.medium.com/max/1000/1*bkFlVrrm4HACGfUzeBnErw.gif" width="80" height="80" />
