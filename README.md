There are many variants of hierarchical clustering; here we explore 3.
The key difference is how you measure the distance between two clusters S<sub>1</sub> and S<sub>2</sub>.
You can click on any of the method names to preview the Jupyter Notebooks online:

[Single-Link](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Single-Link.ipynb): measures the shortest link ![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/4ea47cb29523a267681865d874c59575c56860d0)

[Complete-Link](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Complete-Link.ipynb): measures the longest link ![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/d701e358058dbf66bb18b11a570a089a150ef356)

[Mean-Link](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Mean-Link.ipynb): measures the distances to the means.![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/f41f68299e332d3d7e25ad5518e9933ce91025d3)

[Gonzalez-Algorithm](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Gonzalez.ipynb):  greedy approximation algorithm for finding k clusters that minimize the maximum diameter of a cluster.

[Lloyd's Algorithm](https://nbviewer.jupyter.org/github/TarunSunkaraneni/Clustering/blob/master/notebooks/Lloyd-Algorithm.ipynb)
Consists of two important steps:
1. **Assignment step**: Assign each observation to the cluster whose mean has the least squared Euclidean distance, this is intuitively the "nearest" mean. (partition into the Voronoi diagram by using the means as the "post offices")![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/145a262c93066470be0e062683d64340a1b20121)
2. **Update step**: Calculate the new means to be the centroids of the observations in the new clusters.![alt text](https://wikimedia.org/api/rest_v1/media/math/render/svg/740f4271e822c6400120cb7020ed9cb8439207da)
The algorithm finished when the new means cease to update
