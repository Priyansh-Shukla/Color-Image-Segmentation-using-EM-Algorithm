# Overview

The goal of assignment is to cluster pixels into salient image regions, i.e., regions corresponding to individual surfaces & objects.

Clustering is the task of dividing the population (data points) into a number of groups, such that data points in the same groups are more similar to other data points in that same group than those in other groups. These groups are known as clusters.

k-means clustering algorithm : 
	1.First, randomly select k initial clusters.
	2.Randomly assign each data point to any one of the k clusters.
	3.Calculate the centers of these clusters.
	4.Calculate the distance of all the points from the center of each cluster.
	5.Depending on this distance, the points are reassigned to the nearest cluster.
	6.Calculate the center of the newly formed clusters.
	7.Finally, repeat steps (4), (5) and (6) until either the center of the clusters does not change or we reach the set number of iterations.


## Observation
We implemented the EM and K-means clustering algorithm and used it for intensity segmentation. For smaller values of k the algorithms give good results. For larger values of k, the segmentation is very coarse, many clusters appear in the images at discrete places. This is because Euclidean distance is not a very good metric for segmentation processes.

The quality of the segmentation depends on the image. Smoothly shaded surfaces with clear gray-level steps between different surfaces are ideal for the given algorithms.

k-means works really well when we have a small dataset. It can segment the objects in the image and give impressive results. But the algorithm hits a roadblock when applied on a large dataset (more number of images)

