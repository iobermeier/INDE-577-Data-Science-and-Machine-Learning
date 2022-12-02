# Logistic Regression

Logistic Regression is a supervised learning tool that classifies features to make  predictions. Using independent inputs as variables, the model can predict the outcome of dependent variables. 

There are two main types of regression: 
- Binomial - choose between 2 options
- Multinomal - multiple options to choose 

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205239716-85d1100c-f2c4-43e1-b408-f9ca6ba753d7.png" alt="stochastic" style="width:500px;"/>
</p>

Used in statistics, medical applications, and email sorting, logistic regression makes classifications and enhance decisions through the probability of an event occurring. 

Logistic Regression is easy to implement, efficient to train, and less prone to overfitting. On the other hand, this method can only predict discrete data since it's disjoint nature is the core of the results. 

This unit will primarily focus upon binomial regression using SkLearn's built-in functions instead, but the example could easily include other numeric variables to make predictions. 

## Mathematical Background

Compared to using the equation of a straight line in linear regression, logistic regression uses the sigmoid/logistic function. Since the domain of values of a sigmoid function are close to both 0 and 1, it is appealing for classification. Similar to a natural log, when x = 1, log(x) = 0 ...

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205240300-b458998b-dd1d-4838-bf94-1efe3f2fd809.png" alt="stochastic" style="width:200px;"/>
</p>



## Machine Learning Implementation

To build a logistic regression model, 

## Modeling

[discuss data prep and building the model]

## Understanding the Data
The given dataset downloaded from [kaggle](https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset?resource=download) shows the reviews of 17712 films with details including movie name, review type, score, date, runtime, review, director and actor names. We do not need all the data and process it as described in the modeling section. There are many interpretations that can be done with the data showing correlations, linear relations, and as seen in this notebook, regression modeling.

The outputs of the notebook show that as the audience ratings are likely to be lower than the label of a Fresh or Rotten tomato rating indicates. This may be due to the nuances of the range of values. Since audience ratings are likely to not be 0 or 100, they stay at an average between 40-60 which are hard to relate into either a 0 or 1. Therefore, the Fresh or Rotten tomato ratings are likely not as indicative of the movie quality as the audience ratings.

## References & Further Reading:
- [IBM](https://www.ibm.com/topics/logistic-regression)
- [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2022/01/logistic-regression-an-introductory-note/)
- [Medium](https://medium.com/@toyg_68342/red-wine-quality-classification-with-logistic-regression-8cbe6aa12b67)
