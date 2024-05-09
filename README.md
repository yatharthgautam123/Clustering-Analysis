# Clustering-Analysis

KMeans
Type: Partitioning Clustering
Description:
KMeans divides a dataset into a pre-defined number of clusters, represented by k. Initially, k centroids are randomly chosen from the data points. Iteratively, each data point is assigned to the nearest centroid, forming k clusters. The centroids are then recalculated by taking the mean of all points assigned to each cluster. This process is repeated until the centroids no longer change significantly or a specified number of iterations is reached.

Pros:
Simple and computationally efficient. Works well with large datasets.

Cons:
Requires the number of clusters (k) to be specified beforehand. Sensitive to initial centroid placement.

MeanShift
Type: Density-Based Clustering
Description:
MeanShift doesn't require specifying the number of clusters beforehand. It starts with a set of data points and iteratively shifts each point towards the mean of the points within its neighborhood until convergence. Clusters are formed around high-density regions in the data space. The algorithm automatically determines the number of clusters based on data density.

Pros:
Doesn't require pre-defining the number of clusters. Can handle arbitrary shapes of clusters.

Cons:
Computationally expensive, especially for large datasets. Sensitivity to parameters such as bandwidth.

HClust (Hierarchical Clustering)
Type: Hierarchical Clustering
Description:
HClust builds a hierarchy of clusters. It starts with each data point as a singleton cluster and then merges similar clusters iteratively until all points belong to one cluster. The result is typically visualized using a dendrogram, which illustrates the order in which clusters are merged. Can be agglomerative (bottom-up) or divisive (top-down).

Pros:
Doesn't require specifying the number of clusters beforehand. Provides insights into hierarchical relationships between clusters.

Cons:
Computationally intensive, especially for large datasets. Memory-intensive for storing the hierarchy.

DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
Type: Density-Based Clustering
Description:
DBSCAN groups together points that are closely packed together, based on two parameters: epsilon (ε) - maximum radius of the neighborhood, and minPts - minimum number of points in the neighborhood for a point to be considered a core point. Points within a distance ε of a core point are considered part of the same cluster. Points that are not core points or reachable from core points are classified as noise/outliers.

Pros:
Can identify arbitrarily shaped clusters. Robust to outliers and noise.

Cons:
Sensitivity to parameter tuning, especially ε and minPts. Computationally expensive for large datasets. Each clustering algorithm has its own characteristics, advantages, and limitations, making them suitable for different types of datasets and clustering objectives.

Results for Estimation of obesity levels based on eating habits and physical condition Dataset
KMEANS
name	No Preprocessing	No Preprocessing	No Preprocessing	Norm + PCA	Norm + PCA	Norm + PCA	Norm + PCA + TRANS	Norm + PCA + TRANS	Norm + PCA + TRANS	Normalisation	Normalisation	Normalisation	PCA	PCA	PCA	Transformation	Transformation	Transformation
cluster_size	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5
Silhouette	0.5022	0.474	0.4297	0.1821	0.1415	0.1761	0.1539	0.1617	0.1584	0.1812	0.1402	0.1579	0.5022	0.4739	0.431	0.7405	0.7081	0.6529
Calinski-Harabasz	4716.4535	4798.135	4576.5499	218.7888	202.2217	192.6706	213.7715	193.5156	181.4668	218.811	202.2135	192.8943	4716.4535	4798.1522	4577.5126	91011.4113	83222.2409	93117.9441
Davies-Bouldin	0.6694	0.7016	0.7598	2.2327	2.3849	1.8759	2.417	2.1783	2.417	2.2344	2.381	2.0834	0.6694	0.7022	0.7516	0.4023	0.58	0.5592
meanshift
name	No Preprocessing	No Preprocessing	No Preprocessing	Norm + PCA	Norm + PCA	Norm + PCA	Norm + PCA + TRANS	Norm + PCA + TRANS	Norm + PCA + TRANS	Normalisation	Normalisation	Normalisation	PCA	PCA	PCA	Transformation	Transformation	Transformation
cluster_size	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5
Silhouette	0.5585	0.5585	0.5585	0.285	0.285	0.285	0.293	0.293	0.293	0.285	0.285	0.285	0.5585	0.5585	0.5585	0.9448	0.9448	0.9448
Calinski-Harabasz	4301.3718	4301.3718	4301.3718	27.8296	27.8296	27.8296	33.0076	33.0076	33.0076	27.8296	27.8296	27.8296	4301.3718	4301.3718	4301.3718	88381.1313	88381.1313	88381.1313
Davies-Bouldin	0.5994	0.5994	0.5994	0.7848	0.7848	0.7848	0.7795	0.7795	0.7795	0.7848	0.7848	0.7848	0.5994	0.5994	0.5994	0.0998	0.0998	0.0998
hclust
name	No Preprocessing	No Preprocessing	No Preprocessing	Norm + PCA	Norm + PCA	Norm + PCA	Norm + PCA + TRANS	Norm + PCA + TRANS	Norm + PCA + TRANS	Normalisation	Normalisation	Normalisation	PCA	PCA	PCA	Transformation	Transformation	Transformation
cluster_size	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5
Silhouette	0.4824	0.4735	0.4216	0.1486	0.167	0.1394	0.0954	0.1251	0.1472	0.1486	0.167	0.1394	0.4744	0.4663	0.4161	0.7405	0.7081	0.6529
Calinski-Harabasz	4368.6177	4438.1771	4183.4448	192.5245	177.645	171.1922	180.6725	168.1934	165.8775	192.5245	177.645	171.1922	4285.517	4326.8265	4132.3053	91011.4113	83222.2409	93117.9441
Davies-Bouldin	0.6925	0.6618	0.7339	2.7343	2.7231	2.6463	2.5312	2.8816	2.7323	2.7343	2.7231	2.6463	0.7022	0.669	0.745	0.4023	0.58	0.5592
dbscan
name	No Preprocessing	No Preprocessing	No Preprocessing	Norm + PCA	Norm + PCA	Norm + PCA	Norm + PCA + TRANS	Norm + PCA + TRANS	Norm + PCA + TRANS	Normalisation	Normalisation	Normalisation	PCA	PCA	PCA	Transformation	Transformation	Transformation
cluster_size	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5	3	4	5
Silhouette	-0.5602	-0.5602	-0.5602	-0.2435	-0.2435	-0.2435	-0.2754	-0.2754	-0.2754	-0.2435	-0.2435	-0.2435	-0.5602	-0.5602	-0.5602	-0.4659	-0.4659	-0.4659
Calinski-Harabasz	19.0544	19.0544	19.0544	10.0541	10.0541	10.0541	9.8477	9.8477	9.8477	10.0541	10.0541	10.0541	19.0544	19.0544	19.0544	6.1981	6.1981	6.1981
Davies-Bouldin	1.2283	1.2283	1.2283	1.4235	1.4235	1.4235	1.4414	1.4414	1.4414	1.4235	1.4235	1.4235	1.2283	1.2283	1.2283	1.6331	1.6331	1.6331
