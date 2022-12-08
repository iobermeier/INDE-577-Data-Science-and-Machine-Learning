# Neural Networks

Neural Networks are a supervised learning tool that makes predictions using vectors, layers, node features, and linear regression. Building and training a neural network entails:
1. Generating inputs
2. Making an initial prediction using random weight and bias values
3. Compare the prediction to the actual output
4. Adjust the calculations to predict more accurately

Used in image processing and prediction analysis, neural networks follow a forward and backward propagation to make estimates and build the network. Forward propagation makes the initial guess with multiple hidden layers whereas backward propagation returns to the model and adjusts the calculations to minimize error. As the model compares and adjusts iteratively, it will eventually find the correct values for accurate prediction.

## Mathematical Background

The activation function acts as the driver for each layer and dictates their outputs. Typically, an activation function takes the sum of the weighted input as an argument and returns its output as indicated by a in the following equation:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/206328326-cb57156c-569e-40f1-ba2e-009b02516a0e.png" style="width:200px;"/>
</p>

In this implementation using the Keras framework, we use the rectifier to a linear unit (ReLU) and sigmoid activation functions for the dense layers. The RELU function takes the maximum value from a linear equation y = wx + b and acts like a mini perceptron:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/206322075-4055f40c-208c-487c-afe9-7f59d570fd6f.png" style="width:300px;"/>
</p>

## Machine Learning Implementation

To build a neural network, we use simple units to complete a complex network. Mainly, neurons are split into layers and then apply an activation function. To create the layers for a multi-layer perceptron, we take linear inputs and a bias into a set called a dense layer which gets closer to the predicted output as seen in this diagram:

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/206321451-03ba9ab3-79d0-4687-bc60-cda8aaef7823.png" style="width:300px;"/>
</p>

By stacking the dense layers, we can utilize the Sequential model to generate the predictions.

## Modeling

This implementation using Keras utilizes the Sequential model to connect ordered layers as specified in the machine learning section above.

Using the split, test, train method, we complete the entire ML process for logistic regression. We split the inputs so that 70% is used to train the model and 30% is reserved for testing afterwards.



## Understanding the Data
The given dataset downloaded from the UC Irvine Machine Learning Repository ([UCI](https://archive.ics.uci.edu/ml/datasets/wine+quality)) lists details including acidity, density, pH, sulphates, and alcohol content in both red and white wines to make a quantifiable quality rating. 

The white wine dataset rates 4898 different bottles of wine with 11 columns of details whereas the red wine dataset rates 1599 different bottles, also with 11 columns of details.

The outputs of the notebook show that we can predict which type of wine is more favorable based upon each quality rating. The SkLearn implementation also includes methods in which to test the neural network model by comparing the predicted and actual output values as well as the cost and accuracy for the model.

## References & Further Reading:
- [Kaggle](https://www.kaggle.com/code/ryanholbrook/deep-neural-networks)
- [Geeks for Geeks](https://www.geeksforgeeks.org/activation-functions-neural-networks/?ref=gcse)
- [Real Python](https://realpython.com/python-ai-neural-network/)
