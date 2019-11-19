# Unsupervised learning - lambda clustering

### Lambda - Means
#### 1.1 λ-Means
The K-means clustering algorithm groups instances into K clusters. Each cluster is represented by a prototype vector μk, which represents the mean of the examples in that cluster. Cluster assignments are “hard,” meaning that an instance can belong to only a single cluster at a time.

The K-means algorithm works by assigning instances to the cluster whose prototype μk has the smallest distance to the instance (based on, e.g. Euclidean distance). The mean vectors μk are then updated based on the new assignments of instances to clusters, and this process is repeated using an EM-style iterative algorithm.
A limitation of K-means is that we must choose the number of clusters K in advance, which can be difficult to choose in practice. There is a variant of K-means, which we call λ-means, in which the number of clusters can change as the algorithm proceeds. This algorithm is very similar to K-means, with one difference: when assigning an instance xi to a cluster, we will assign it to the lowest-distance cluster unless all of the clusters have a distance larger than some threshold λ. In this case, we then assign xi to a new cluster, which is denoted cluster K + 1 if we previously had K clusters. The prototype vector for the new cluster will simply be the same vector as the instance, μK+1 = xi. The idea is that if an instance is not similar to any of the clusters, we should start a new one.

This algorithm (called “DP-means” here) is described in: B. Kulis and M.I. Jordan. Revisiting k-means: New AlgorithmsviaBayesian Nonparametrics.29thInternationalConferenceonMachineLearning(ICML),2012.
(https://arxiv.org/abs/1111.0352)


#### Execute the code
Simply run `k_means_EM.ipynb` in order.

Helper functions:

`read_data`: read txt files. Note that this function only applies to the first (numerical) dataset.
`DPmeans.calc_lambda`: default lambda, the largest Euclidean distance between two points in a dataset.
`DPmeans.train`: The train method learns the cluster parameters from the data. The result of the train method are the cluster parameters: the means μk and the number of clusters K.
`DPmeans.predict`: The predict method labels the examples by assigning them to the closest cluster. The value of the label is the cluster index, i.e., an example closest to kth cluster should receive label k.


![2d_visual](https://github.com/yanb514/ML_programming_assignments/blob/master/4_unsupervised_learning/2d_visual.png)
Visualize clustering in 2-D

#### Optimal lambda:
32-D Gaussian dataset: 0.3-1.2
water-treatment dataset: 1
