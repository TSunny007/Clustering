You can click on any of the method names to preview the Jupyter Notebooks online:

**Agglomerative**: This is a "bottom up" approach: each observation starts in its own cluster, and pairs of clusters are merged as one moves up the hierarchy. Each of these "links" measure distance between clusters differently, and every step clusters are combined on the basis of which of the clusters are *closest (least distant)*.

There are many variants of hierarchical clustering; here we explore 3.
The key difference is how you measure the distance between two clusters S<sub>1</sub> and S<sub>2</sub>.

[Single-Link](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Single-Link.ipynb): inter-cluster *distance* is measured by the shortest link (distance between the closest set of points from cluster *A* to *B*) ![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/4ea47cb29523a267681865d874c59575c56860d0)

[Complete-Link](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Complete-Link.ipynb): inter-cluster *distance* is measured by the longest link (distance between the furthest set of points from cluster *A* to *B*)![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/d701e358058dbf66bb18b11a570a089a150ef356)

[Mean-Link](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Mean-Link.ipynb): measures inter-cluster *distance* is measured by the mean link (distance between the center of masses of cluster *A* and *B*) ![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/f41f68299e332d3d7e25ad5518e9933ce91025d3)

---

[Gonzalez-Algorithm](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Gonzalez.ipynb):  Greedy approximation algorithm for finding k clusters that minimize the maximum diameter of a cluster. This essenatially tries to pick cluster points as the furthest point from all other cluster center points. Chokes with outliers.

---

**Centroid-based**: Optimizes finding the k cluster centers and assign the objects to the nearest cluster center, such that the squared distances from the cluster are minimized. Chokes with bad initial centeroid initialization.

[Lloyd's Algorithm *(K-means)*](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Lloyd-Algorithm.ipynb)
Consists of two important steps:
1. **Assignment step**: Assign each observation to the cluster whose mean has the least squared Euclidean distance, this is intuitively the "nearest" mean. (partition into the Voronoi diagram by using the means as the "post offices")![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/145a262c93066470be0e062683d64340a1b20121)
2. **Update step**: Calculate the new means to be the centroids of the observations in the new clusters.![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/740f4271e822c6400120cb7020ed9cb8439207da)

The algorithm finishes when the new means stop changing with new iterations.

