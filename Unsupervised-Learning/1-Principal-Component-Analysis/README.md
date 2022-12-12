# Principal Component Analysis

Principal Component Analysis (PCA) is an unsupervised learning tool within dimensionality reduction that helps reduce the size of large datasets to make them more compact for further processing. As seen in the following image, dimensionality reduction is needed since model performance steeply declines with too many features.

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/206976033-8125f74d-6aa0-4d0a-8667-4405dbf16163.png" style="width:500px;"/>
</p>

Used in pre-processing, image reduction, and pattern recognition, dimensionality reduction maps a higher dimensional feature space to a lower dimensional feature space. PCA specifically hopes to retain as much information of the original dataset. The results from the PCA are the linear combinations of the numerical inputs called principal components (PC) and are orthogonal so that the first PC will contain most of the variance of the data and reduce as more dimensions are condensed.

This unit will first implement a basic demonstration with artificial data followed by a comparison using real data. There will be a third implementation using SkLearn to plot the output of the clusters.

## Mathematical Background & Machine Learning Implementation

PCA is guided by feature extraction and uses eigenvalue decomposition of a covariance matrix with the follow steps:
1. Calculate the covariance matrix
<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/206978823-4809a2c2-6da0-4731-8364-151692d7bcbe.png" style="width:300px;"/>
</p>

2. Calculate the eigenvectors of the covariance matrix
3. The eigenvector with the highest eigenvalue indicates the direction of highest variance
   * this is the location of the first PC
4. Use the same process to find the second PC
5. Repeat until k PCs are identified

## Modeling

Using SkLearn's 'PCA' library, we define the number of components/dimensions we want to keep and calculate the directions of highest variance. The output of this function is the variance of each column and a condensed new data frame.

## Understanding the Data
The artificial dataset was generated using NumPy's RandomState for a matrix with size 200 x 2. Since the input is an oblong shape, we want to find its center. The output of the PCA on the artificial dataset shows the direction of variance from the calculated center.

For the real data, the given dataset downloaded from the UC Irvine Machine Learning Repository (UCI) describes both red and white wine to make a quantifiable quality rating. Both datasets rate 1599 different bottles, with 13 columns of details including acidity, density, pH, sulphates, and alcohol content. Rather than graphing the directionality or the quality of the wine (since this was done in a previous notebook), we simply prove that the dimensionality shows no correlations.

The final implementation of PCA uses [SkLearn's 'load_diabetes'](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_diabetes.html#sklearn.datasets.load_diabetes) dataset with a size of 442 rows of samples and 10 columns of patient info and samples. Its outputs show the distribution of variances after running the PCA, with favorable results.

## References & Further Reading:
- [GeeksForGeeks](https://www.geeksforgeeks.org/reduce-data-dimentionality-using-pca-python/) - Reduce Data Dimensionality
- [GeeksForGeeks](https://www.geeksforgeeks.org/mathematical-approach-to-pca/) - Mathematical Approach to PCA
- [Towards Data Science](https://towardsdatascience.com/dimension-reduction-techniques-with-python-f36ca7009e5c)
