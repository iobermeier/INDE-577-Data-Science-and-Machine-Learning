# Decision/Regression Trees

Decision and regression trees are a supervised decision tool that uses a tree-like flowchart to segment decisions until a final outcome. Upon each decision which follows the if-then format, there is a branch to a new set of tests or the final result. Each decision is referred to as a leaf, with the starting point referred to as the root.

Used in operations research and management, decision trees are represented by 3 types of nodes
1. Decision nodes - squares/leaf
2. Chance nodes - circles
3. End nodes - triangles

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207300083-f6ee686f-ce88-4e20-8440-485269c53f52.png" style="width:500px;"/>
</p>

In contrast, regression trees use continuous values to predict outputs similar to classification/decision trees. The main drawback that makes regression trees unfavorable compared to decision trees is that they are prone to overfitting. Using cross validation methods and specifying the minimum number of nodes a leaf can have can help deter overfitting.

This unit will primarily focus upon implementing decision trees and evaluating its accuracy but will also give a glimpse into using regression trees with a comparative accuracy.

## Mathematical Background & Machine Learning Implementation
A decision tree is constructed by splitting the staring/source into subsets based upon a specific attribute. By repeating this process, we complete recursive partitioning until splitting is no longer necessary. 
### Decision Trees

To increase homogeneity, we continuously calculate the entropy/impurity of a node using the following equation. By implementing the correct tests, entropy is naturally reduced, therefore allowing the model to ask fewer questions.

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207302592-e068b5c4-a6fa-4a73-b913-c6ba53ebc329.png" style="width:350px;"/>
</p>

To determine the correct tests to reduce entropy, we calculate features from the input dataset using a process called information gain. By calculating the difference between the entropy of the parent and the sum of the entropy of the child test. Whichever feature receives the highest information gain is chosen as the next test to split the data into the next branch. 

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207304455-ebf575d5-c715-4956-8021-ed07fbd19efc.png" style="width:700px;"/>
</p>

### Regression

Regression cannot follow the same mathematical calculations such as entropy due to the continuous nature of the input data. Therefore, to predict values, we use mean square error to reduce homogeneity. In the following equation, Y is the actual value, and Y_hat is the predicted value. The rest of the regression algorithm mimics the information gain computation done in decision trees until the tests are exhausted.

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/207305260-3c555bd9-06fb-4189-8ff9-08ac4f4c6c9c.png" style="width:300px;"/>
</p>

## Modeling

Using the split, test, train method, we complete the entire ML process for both decision and regression trees. We split the inputs so that 80% is used to train the model and 20% is reserved for testing afterwards. Due to the nature of the everchanging format, fitting is required to keep the model cohesive.

Further accuracy models such as decision regions are used to help visualize the graphical areas of how the decisions are impactful.

## Understanding the Data
This unit uses the 'load_wine' dataset from [SkLearn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html#sklearn.datasets.load_wine) which contains 178 rows, with 13 columns of features including magnesium, ash, flavanoids, and color intensity of the three types of wine: white, red, and blends.

The outputs of the notebook show a fully classified decision tree, decision regions, and a confusion matrix fully analyzing the decision tree accuracy, which performs quite well. A regression tree is also trained and calculates the accuracy, which performs well, yet is not as precise as the decision tree model.

## References & Further Reading:
- [Wikipedia](https://en.wikipedia.org/wiki/Decision_tree) - Decision Trees
- [scikit Learn](https://scikit-learn.org/stable/modules/tree.html)
- [Medium](https://medium.com/analytics-vidhya/decision-trees-for-classification-id3-machine-learning-6844f026bf1a) - Decision Trees for Classification
