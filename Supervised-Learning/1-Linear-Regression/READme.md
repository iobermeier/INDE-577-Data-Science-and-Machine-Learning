# Linear Regression

Linear regression is a supervised learning tool that uses predictive analysis to demonstrate the relationship of dependent variable to an independent variable. This relationship estimates unknown model parameters from the given data for improved linear predictor functions. 

Used in research, results prediction, and trend forecasts, linear regression models are fueled by solving a least squares equation such as y = mx + b. Linear regression algorithms use 'x' as the input and 'y' as the dependent variable to solve for the slope, 'm' and the y-intercept, 'b'. 
Linear regression has applicability in artificial intelligence, finance, economics, and many other fields that rely upon prediction models.

## Mathematical Background
### Linear Activation Function:


### Mean Squared Error / Cost Function: 
Minimizes the error between the predicted and actual values. More specifically, after calculating the distance between a data point and the regression line, it is then squared, and sum over all data points. The resulting value is the benchmark to which the ordinary least squares want to minimize which eventually estimates the linear coefficients.

![Cost Function](https://github.com/iobermeier/INDE-577-Data-Science-and-Machine-Learning/blob/main/Supervised-Learning/1-Linear-Regression/images/Cost%20Function.png)

### Gradient Descent
Minimizing the error of the cost function by iteratively reducing the cost helps indicate how to change the values. Even though the cost function can compute local minima, linear regression always outputs absolute minima, aka a convex function.

The gradient descent computes partial derivatives to help dictate the learning rate in which the algorithm converges to the minima as seen in the image below. The partial derivatives update the input values with alpha as the learning rate. A small alpha indicates a close minima that takes more time to reach, whereas a large alpha is farther (converges more quickly), but can accidentally overshoot the minima. Therefore, it is importantly to pick the correct alpha/learning rate. 

![Gradient Descent](https://github.com/iobermeier/INDE-577-Data-Science-and-Machine-Learning/blob/main/Supervised-Learning/1-Linear-Regression/images/Gradient%20Descent.png)

The output of the Cost Function gives the coefficients needed for modeling linear regression.

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
(describe what the results of this dataset show)

## References & Further Reading:
- [Wikipedia - Linear Regression](https://en.wikipedia.org/wiki/Linear_regression)
- [IBM Linear Regression](https://www.ibm.com/docs/en/db2oc?topic=procedures-linear-regression)
- [Towards Data Science](https://towardsdatascience.com/introduction-to-machine-learning-algorithms-linear-regression-14c4e325882a)
