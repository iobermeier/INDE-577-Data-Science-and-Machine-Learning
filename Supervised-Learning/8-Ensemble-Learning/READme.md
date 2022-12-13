# Ensemble Learning

Ensemble Learning is a supervised learning tool that creates improved predictions over any of the previous learning methods that have been implemented so far. Using a finite set of models, there is increased flexibility to analyze inputs. Used in remote sensing, computer security, and fraud detection, ensemble learning builds upon previous classifications to select the optimal option based upon the data.

There are three main methods of ensemble learning:
1. BAGGing - also known as Bootstrap AGGregating - generates sets with randomly chosen elements that omits one of the original sets, then runs decision trees on the bootstrapped set

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207312321-44cb3d93-278b-499c-8cf5-ca32768a9a0d.png" style="width:300px;"/>
</p>

2. Random Forests - collections of decision trees to compute an increased accuracy than a single tree

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207312586-94b2a3a3-6019-4dc0-a7ed-b6af62145726.png" style="height:300px;width:300px;"/>
</p>

3. Boosting - adds samples sequentially that adjust predictions recursively based upon prior model outputs

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207312685-d54c4498-f0dd-49d5-b33c-cb6aeaabc4c0.png" style="width:300px;"/>
</p>

This unit will primarily focus upon the outputs and accuracy assessments of bagging and random forests implementations. 

## Machine Learning Implementation

Using SkLearn's libraries, we use the 'Bagging Classifier' and 'Decision Tree Classifier' for the Bagging implementation and the 'Random Forest Classifier' for the Random Forest implementation to generate our models.

## Modeling

To choose the most appropriate model, consider 1, the type of classifier is best suited, and 2, by using a specific classifier, does it provide consistent results? Commonly, classifiers with the smallest errors or smallest averaged error from the training data are used. Using the split, test, train method, we complete the entire ML process for ensemble learning. We split the inputs so that 70% is used to train the model and 30% is reserved for testing afterwards.

In bagging, the model uses the bootstrapped set for training which will eventually become the ensemble. Similarly, random forests generate multiple trees, but condense the model to output a single result.

## Understanding the Data
As used in most of the classification units prior, this unit uses the 'load_wine' dataset from [SkLearn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html#sklearn.datasets.load_wine) which contains 178 rows, with 13 columns of features including magnesium, ash, flavanoids, and color intensity of the three types of wine: white, red, and blends. To better manage and visualize the data, we restrict the inputs to the first 100 data points. 

The outputs of the notebook show a horizontally segmented decision region for bagging with an accuracy ranging between 82 - 89%. The output for random forests has a single feature covering the left half of the decision region graph, with the other two features to the right, one on top of the other. The random forest accuracy ranges between 88% - 92%, a bit better than the bagging method. Based on these results, it would be deduced that the random forests method is a slightly better implementation to use when further testing the inputs.

## References & Further Reading:
- [Wikipedia](https://en.wikipedia.org/wiki/Ensemble_learning) - Ensemble learning
- [A Gentle Introduction to Ensemble Learning Algorithms](https://machinelearningmastery.com/tour-of-ensemble-learning-algorithms/)
- [Towards Data Science](https://towardsdatascience.com/ensemble-methods-in-machine-learning-what-are-they-and-why-use-them-68ec3f9fef5f)
