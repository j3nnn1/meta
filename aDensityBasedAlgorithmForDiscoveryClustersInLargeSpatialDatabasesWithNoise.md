## A Density-Based Algorithm for Discovering Clusters in Large Spatial Databases with Noise
## Martin Ester, Hans Peter kriegel, Jorg Sander, Xiaowei Xu


## Dbscans with geospacial databases.
* search for using synthetic data and real data of the SEQUOIA 2000 bench- mark.
* Dbscan > Kmeans or Clarans: cluster shape and best performance.
* minimal requirement of domain knowledge to determine the input parameters.

### intro clustering.
- clustering partitioning
- clustering hierarchical

Partitional clustering: for a D dataset of n objects, split in k cluster.
k is a input parameter.
two step procedure, (use a gravity center, medoides o centroides)

Hierarchical clustering: create a hierarchical decomposi- tion of D. The hierarchical decomposition is represented by a dendrogram, a tree that iteratively splits D into smaller subsets until each subset consists of only one object. So far, the main problem with hierarchical clustering al- gorithms has been the difficulty of deriving appropriate pa- rameters for the termination condition, e.g. a value of Dmin which is small enough to separate all “natural” clusters and, at the same time large enough such that no cluster is split into two parts.




