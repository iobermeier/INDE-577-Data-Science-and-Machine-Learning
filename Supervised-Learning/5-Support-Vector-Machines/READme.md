# Support Vector Machines

Support Vector Machines (SVM) are a supervised learning tool used for classification, regression, and detection of outliers. Using inputs that are assigned to at least two different classes, SVM models can classify the data based on non-probabilistic binary linearity. Used in text categorization, image classification, and recognition tools, SVMs, aim to maximize the gap between two classes and then map predicted data into those classifiers.

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207224853-e1df1b97-2bb0-4a97-ba72-f1a3e7e39d3f.png" style="width:200px;"/>
<img src="https://user-images.githubusercontent.com/97500105/207225370-d4c2cfcd-279a-4c68-9eee-053479f2ceaf.png" style="width:200px;"/>
</p>

Even though SVMs are primarily a supervised learning algorithm, it also contains a sub method known as support vector clustering to handle unlabeled data, ie unsupervised data. The process is about the same as SVMs, but internally assigns temporary labels for processing.

This unit will primarily focus upon linear processing of SVMs and compare skLearn's functions for implementation.

## Mathematical Background

SVMs use the output of a linear function, either 1 or -1 and create a threshold value which acts as a margin for the decision boundaries

Linear SVMs create either a hard or soft margin:
- Hard margin - linearly separable to using the distance equations that classify whether a data point is in one class or another:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207223756-1f006fa6-d221-41d3-9c58-fa7cbfcfaa79.png" style="width:600px;"/>
</p>

- Soft margin - not linearly separable, uses the hinge loss function to categorize the margin classification (=1 if on the correct side of the margin):

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207223993-75de1e3b-c5e3-42c8-b7d3-d99a0005dfa8.png" style="width:200px;"/>
</p>

## Machine Learning Implementation

As previously mentioned, SVMs are used in machine learning as non-probabilistic, linear, binary classifiers by learning the hyperplane separating the inputs. While classification is straightforward, unlabeled data can use the kernel trick to still apply SVMs. The kernel trick projects inputs to a higher dimension in which they become linearly separable and can then be processed as though it were originally a linear dataset.

## Modeling

Using skLearn's svm and Decision Boundary Display libraries, as well as the split, test, train method, we complete the entire ML process for SVM implementation. We split the inputs so that 70% is used to train the model and 30% is reserved for testing afterwards. First we split the data, then fit the SVM model, and display the boundaries.

## Understanding the Data
We use the 'load_wine' dataset from [SkLearn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html#sklearn.datasets.load_wine) to compare the inputs to the previously used external wine dataset from UCI. This wine dataset is much smaller and contains only 178 rows, with 13 columns of slightly different features including magnesium, ash, flavanoids, and color intensity of three wine types: white, red, and blends. We want to compare and analyze the alcohol content and flavanoids within the dataset. We also append the target vector from skLearn to the data for cohesion when processing.

The outputs of the notebook show the calculated boundary for the various wine types in the data. When comparing two types of skLearn SVM functions, 'SVC' and 'LinearSVC', we calculate a greater accuracy for 'SVC' by a few percent. 

## References & Further Reading:
- [scikit Learn](https://scikit-learn.org/stable/auto_examples/svm/plot_iris_svc.html) - Plotting SVM Classifiers
- [scikit Learn](https://scikit-learn.org/stable/auto_examples/svm/plot_separating_hyperplane.html#sphx-glr-auto-examples-svm-plot-separating-hyperplane-py) - Maximum Margin Separating
- [Wikipedia](https://en.wikipedia.org/wiki/Support_vector_machine#Linear_SVM) - Support Vector Machines
