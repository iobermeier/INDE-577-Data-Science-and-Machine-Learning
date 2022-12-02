# Logistic Regression

Logistic Regression is a supervised learning tool that classifies features to make  predictions. Using independent inputs as variables, the model can predict the outcome of dependent variables. 

There are two main types of regression: 
- Binomial - choose between 2 options
- Multinomial - multiple options to choose 

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205239716-85d1100c-f2c4-43e1-b408-f9ca6ba753d7.png" alt="logreg" style="width:500px;"/>
</p>

Used in statistics, medical applications, and email sorting, logistic regression makes classifications and enhance decisions through the probability of an event occurring. 

Logistic Regression is easy to implement, efficient to train, and less prone to overfitting. On the other hand, this method can only predict discrete data since its disjoint nature is the core of the results. 

This unit will primarily focus upon binomial regression using SkLearn's built-in functions instead, but the example could easily include other numeric variables to make predictions. 

## Mathematical Background

Compared to using the equation of a straight line in linear regression, logistic regression uses the sigmoid/logistic function. Since the domain of values of a sigmoid function are close to either 0 or 1, it is appealing for classification.

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205240300-b458998b-dd1d-4838-bf94-1efe3f2fd809.png" alt="sigmoid" style="width:200px;"/>
</p>

f(x) is often considered to have a probability of 1 and so 1 - f(x) is considered to have an output to 0. Similar to a natural log, when x = 1, then log(x) = 0 and log(1 - x) is always approaching 1, therefore creating the following graphical behavior:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205260985-23dde321-cd39-4c9b-8690-d0dbbe3f8a91.png" alt="sigmoid graph" style="width:400px;"/>
</p>

Building upon principles from previous units, the application of the sigmoid function in conjunction with gradient descent and cost calculations follow a process similar to linear regression. Rather than observing the results for linear results, we hope to have parabolic behavior.

## Machine Learning Implementation

To build a logistic regression model, we want to build a model that returns values as similar to the actual values, either 0 or 1. The process in which to process the inputs into binomial outputs, follows a 3-step process known as the perceptron. 
1. Take inputs and multiply by weights that are calculated by maximum likelihood calculations
2. Sum the products from step 1 into a weight sum
3. The weighted sum is applied to the activation function that sets thresholds for the outputs

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205265065-96f14665-520d-4e64-b66f-2a5984af548b.png" alt="perceptron" style="width:600px;"/>
</p>

The weights in the perceptron are one of the most important steps since it can demonstrate the strength of the input value (node).

## Modeling

Using the split, test, train method, we complete the entire ML process for logistic regression. We split the inputs so that 70% is used to train the model and 30% is reserved for testing afterwards.

After logistic regression is modeled, we analyze its accuracy through binary classifiers such as:
- positive predictive values: ratio of true +s : total +s
- negative predictive values: ratio of true -s : total -s
- sensitivity: ratio of true +s : actual +s
- specificity: ratio of true -s : actual -s

The results of such analysis can be represented in a confusion matrix that separates such values into quadrants and visualizes the ratios of true and actual values.

## Understanding the Data
The given dataset downloaded from [kaggle](https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset?resource=download) shows the reviews of 17712 films with details including movie name, review type, score, date, runtime, review, director and actor names. We do not need all the data and process it as described in the modeling section. There are many interpretations that can be done with the data showing correlations, linear relations, and as seen in this notebook, regression modeling.

The outputs of the notebook show that as the audience ratings are likely to be lower than the label of a Fresh or Rotten tomato rating indicates. This may be due to the nuances of the range of values. Since audience ratings are likely to not be 0 or 100, they stay at an average between 40-60 which are hard to relate into either a 0 or 1. Therefore, the Fresh or Rotten tomato ratings are likely not as indicative of the movie quality as the audience ratings.

## References & Further Reading:
- [IBM](https://www.ibm.com/topics/logistic-regression)
- [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2022/01/logistic-regression-an-introductory-note/)
- [Medium](https://medium.com/@toyg_68342/red-wine-quality-classification-with-logistic-regression-8cbe6aa12b67)
