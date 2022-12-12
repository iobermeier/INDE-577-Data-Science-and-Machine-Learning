# k-Means Clustering

k-Means Clustering is an unsupervised learning tool that clusters data according to n groups of samples with equal variance. One of many clustering methods, the primary algorithms fall into one of the following 3 categories:
1. Partitional - nonoverlapping groups
   * k-means falls into this category
2. Hierarchical - builds either top-down (divisive) or bottom-up (agglomerative)
3. Density-Based - groups based on density of a region

Used in medical and customer satisfaction, k-means identifies meaningfulness and usefulness, or more specifically expands the domain of knowledge and acts as an intermediate data preparation step.


This unit will implement a simple example of k-means using artificial data and real image data followed by an accuracy analysis.

## Mathematical Background

The main purpose of the k-means algorithm is to divide N samples X into K disjoint clusters C with a mean of the samples in the cluster, aka centroids. To choose the centroids, the within-cluster sum-of-square criterion, aka inertia, is a minimization of the difference of inputs versus mean squared.

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/206968748-a11c511a-ddb3-4b81-b2df-10dc4057bdd6.png" style="width:200px;"/>
</p>

## Machine Learning Implementation

Using Lloyds's algorithm k-means follows 3 primary steps:
1. Choose initial centroids, typically k samples from dataset
2. Assign each sample to the nearest centroid
3. Take the mean of the samples assigned to the centroids and create a new centroid

These steps are repeated until the variance is minimized. 

Written clearly, k-means follows this pseudocode:
<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/206970396-f3d46387-515e-4097-b918-f6977dd1fbb3.png" style="width:500px;"/>
</p>

## Modeling

Using SkLearn's 'KMeans' library, we define the number of clusters we want and test the accuracy of the initial guess and adjust as necessary. The outputs of the clustered data are typically separate from one another since we are using the partitional application, and is color coordinated to point out the difference. KMeans is a convenient intermediary algorithm that can prepare datasets for more accurate results when used in other applications such as Logistic Regression.


## Understanding the Data
The artificial dataset was generated using [SkLearn's 'make_blobs'](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_blobs.html) dataset with a size of 300 x 4. Its outputs show the color-coordinated clusters as well as the centroid calculations and plotting.

We use an image of the Rice Quad for the real implementation that has a size of 1080 x 720 pixel which is scaled down to accommodate the color ranges of RGB. The output of the clustered image is seen in a filtered image that splits the colors into as many k categories as specified. In this notebook, we specify 3 colors, therefore we see blue, white/tan, and green in the output.


## References & Further Reading:
- [Real Python](https://realpython.com/k-means-clustering-python/)
- [SciKit Learn](https://scikit-learn.org/stable/modules/clustering.html#k-means)
