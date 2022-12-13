# k-Nearest Neighbors

k-Nearest Neighbors (kNNs) is a supervised learning tool that handles classification (discrete) and regression (continuous) of data to predict features based upon the neighboring nodes. Using a k number of specified samples closest to the chosen point (determined by the distance equation), the model can predict its label.

<p align="center">
<img src="https://robocrop.realpython.net/?url=https%3A//files.realpython.com/media/knn_02_MLsupervised_wide.aa50e6348ca4.png&w=756&sig=518b3367cb99f63624ccea571df3089ba558ea9e" style="width:500px;"/>
</p>

Used in processing satellite images and predicting handwriting, kNN considers model complexity for high dimensional datasets, but performs poorly for low quantity datasets. This unit will primarily focus upon the nearest neighbor algorithm for 2 different data types to prove the importance of data rich datasets.

## Mathematical Background
One of the instrumental pieces of computing the nearest neighbors includes finding the points nearest to that of interest. In order to so, we calculate the Euclidean distance between the point of interest and its neighbors using the following equation:

<p align="center">
<img src="" style="width:300px;"/>
</p>

Take the k most minimum numbers, we have a guess at what the label would be for the point of interest.

## Machine Learning Implementation

Steps to perform kNN:
1. Split data into test and training data
2. Compute k-nearest neighbor algorithm
   * choose the number of neighbors (min of 1)
   * use data point features to calculate the distance between points
   * find the k minimum distances to the chosen point
   * take the mode, aka what occurs most often, as the prediction label
3. Generate the model using the neighbor features
4. Train and fit the model
5. Predict the label


## Modeling

Using the split, test, train method, we complete the entire ML process for kNN. We split the inputs so that 70% is used to train the model and 30% is reserved for testing afterwards.

Further fitting of the data is necessary for the scaling of the split dataset

## Understanding the Data
This unit uses two different datasets to compare the effectiveness of the kNN. 
The first is the 'load_wine' dataset from [SkLearn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html#sklearn.datasets.load_wine) which contains 178 rows, with 13 columns of features including magnesium, ash, flavanoids, and color intensity of the three types of wine: white, red, and blends. Two additional columns are appended; one for the numerical target, and a second to set the name of the wine type.

The outputs of the model using the wine dataset consistently gives a correct classification for the type of wine that is being evaluated. As we increase the number of k neighbors, the loss of the model decreases, and the accuracy increases.

The second dataset downloaded from [GitHub](https://github.com/susanli2016/Machine-Learning-with-Python/blob/master/fruit_data_with_colors.txt) was gathered by Dr. Iain Murray from the University of Edinburgh and has 58 rows of various fruit types including apples, oranges, mandarins, and lemons with 7 columns of details including mass, color score, and fruit subtype.

The outputs of the model using the fruits dataset performed worse than expected. While the particular point we chose gave the correct classification, the accuracy ratings are either 2/3 or 1/2. Since this probability is close to flipping a coin, we ran the model on this dataset again using a different datapoint which yielded completely inaccurate results in which the neighbors and predicted label were all lemon even though the chosen label was mandarin. In this test, the distance between 2 neighbors was 34, which is much higher than that of the first two model tests which ranged between 0.1 and 2.0. The extreme distance between the neighbors is likely the cause of the misclassification.

Since we have run the model on the wine dataset, we know that the model itself can yield highly accurate results and indicates the importance of choosing the right dataset for each algorithm. In the future, the fruit dataset would not be the best to test kNN but is a good analysis test.

## References & Further Reading:
- [Scikit Learn](https://scikit-learn.org/stable/modules/neighbors.html)
- [Real Python](https://realpython.com/knn-python/)
