# Linear Regression

Linear regression is a supervised learning tool that uses predictive analysis to demonstrate the relationship of dependent variable to an independent variable. This relationship estimates unknown model parameters from the given data for improved linear predictor functions. 

Used in research, results prediction, and trend forecasts, linear regression models are fueled by solving a least squares equation such as y = mx + b. Linear regression algorithms use 'x' as the input and 'y' as the dependent variable to solve for the slope, 'm' and the y-intercept, 'b'. 
Linear regression has applicability in artificial intelligence, finance, economics, and many other fields that rely upon prediction models.

## Mathematical Background



## Machine Learning Implementation

To build a linear regression model, there are a number of methods and tools we can use. One way is to hard code the model from the mathematical equations previously mentioned using the NumPy library. While this is a good exercise, it is much more streamlined to use libraries that already compute linear regression models. One of these predetermined methods is to use the scikit learn library, specifically the 'LinearRegression' dependency from the 'linear_model' sub-library.

## Modeling

Since both the input and output values are real numeric values, linear regression is a favorable modeling technique. The best fit straight line demonstrates the linear relationship between our input variables based upon the linear equation of a line as mentioned above. The model is fit based upon training data and outputs the predicted values. 

To ensure that the input data will be properly modeled using linear regression, we need to prepare the inputs. 
1. One needs to ensure that the raw data has a linear relationship rather than something like an exponential relationship, which would need a log transform to become linear. 
2. The data should not be noisy and should consider removing outliers since this can skew the prediction models. 
3. Rescaling the inputs using standardization or normalization can ensure more reliable and precise models. 

After the data is modeled, we can further calculate mathematical properties such as mean, standard deviation, correlation, and covariance.


## References & Further Reading:
- Wikipedia - Linear Regression 
- IBM Linear Regression
- Towards Data Science
