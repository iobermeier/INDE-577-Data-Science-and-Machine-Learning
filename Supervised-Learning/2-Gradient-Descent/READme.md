# Gradient Descent

Gradient Descent is a supervised learning tool that optimizes results by minimizing cost functions as much as possible. A gradient is essentially the slope of a function or a partial derivative that accounts for the change in weights relative to the change in error.

Used in research to test accuracy, gradient descent models are trained upon convex functions that will iteratively find a local minimum, aka when the slope becomes 0. An initial guess or starting point is set and iteratively adjusts based upon values of alpha that will minimize the cost function. As seen with its applicability in the Linear Regression lesson, gradient descent is a foundational training algorithm for machine learning.

### Stochastic Gradient Descent
Stochastic, meaning a process done with random probability, randomly selects a few samples for each iteration. The gradient is computed of a single sample instead of the sum of all gradients durig each iteration. Due to the random sampling, the process is generally a bit noisier, as seen with this representation of finding the center/minimum:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/204724664-7c60af84-6da7-46a8-9d17-777319292e25.jpeg" alt="stochastic" style="width:300px;"/>
</p>

### Batch Gradient Descent
Batch, meaning using all the data from a dataset, trains so that the descent is less noisy and predictable. This method is not recommended with large datasets since it is computational expensive. In contrast to stochastic, finding the minimum is a smoother, yet longer process:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/204724693-69197675-a63b-4563-a090-2fb86a09d2f4.png" alt="batch" style="width:300px;"/>
</p>

## Mathematical Background

When using the equation of a line, y = mx + b, we need to solve a system of equations to get the values of m and b. In terms of machine learning, we can consider the equation of a line through the cost function J in which b = theta0 and m = theta1:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/204717304-1ae37392-429d-4452-a5f3-4c7b8ec48567.png" alt="J equation";"/>
</p>
Mathematically, each gradient is the partial derivative of the cost function for each iteration of the model (seen as m below):

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/204717568-bc7bb4e4-d0fd-4c79-9a9c-b8b898229f08.png" alt="cost partials";"/>
</p>

To calculate the value of each theta/gradient, we iteratively calculate the difference between the first chosen value of theta and the rate of descent. The rate of descent computes the sum of differences between the predicted and current equations:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/204723775-3f5014e6-9572-41b0-bdd7-19dcceb53e9b.png" alt="gradients";"/>
</p>


## Machine Learning Implementation

To build a linear regression model, there are a number of methods and tools we can use. One way is to hard code the model from the mathematical equations previously mentioned using the NumPy library. While this is a good exercise, it is much more streamlined to use libraries that already compute linear regression models. One of these predetermined methods is to use the scikit learn library, specifically the 'LinearRegression' dependency from the 'linear_model' sub-library.

## Modeling

Since both the input and output values are real numeric values, linear regression is a favorable modeling technique. The best fit straight line demonstrates the linear relationship between our input variables based upon the linear equation of a line as mentioned above. The model is fit based upon training data and outputs the predicted values. 

To ensure that the input data will be properly modeled using linear regression, we need to prepare the inputs. 
1. One needs to ensure that the raw data has a linear relationship rather than something like an exponential relationship, which would need a log transform to become linear. 
2. The data should not be noisy and should consider removing outliers since this can skew the prediction models. 
3. Rescaling the inputs using standardization or normalization can ensure more reliable and precise models. 

After the data is modeled, we can further calculate mathematical properties such as mean, standard deviation, correlation, and covariance.

## Understanding the Data
The given dataset downloaded from [kaggle](https://www.kaggle.com/datasets/himanshunakrani/student-study-hours?resource=download) plots the amount of hours a student studied for a test compared to the grade they received. Having used the same data set for calculating gradient descent in the Linear Regression unit, we know that this data is fit and able to exemplify this topic. 

## References & Further Reading:
- [Wikipedia - Gradient Descent](https://en.wikipedia.org/wiki/Gradient_descent)
- [Built In](https://builtin.com/data-science/gradient-descent)
- [GeeksForGeeks](https://www.geeksforgeeks.org/difference-between-batch-gradient-descent-and-stochastic-gradient-descent/)
- [Towards Data Science](https://towardsdatascience.com/gradient-descent-in-python-a0d07285742f)
