<H1 align="center">Binary Logistic Regression from Scratch for Iris Dataset</H1>

- In this repository I have implemented Binary Logistic Regression from Scratch for Iris Dataset in python and then use Iris dataset to test and train the model using one vs all method for each class.
- I have created three different dataset and created 3 different models fot these dataset. I have also calculated accuracy for these models.

# Steps for creating training the model:
1.  We build our hypothesis.
2.  Randomly initialize parameters.
3.  Create Loss function
4.  Find local derivative of loss function.
5.  Apply gradient descent to update the weights.
6.  Repeat 4 and 5 step unless epochs are finished or our loss is close to zero.

# Pre-processing the dataset:

- As we are going to use only numpy, so, we have to convert the data X, Y to arrays. I also inserted a column in X of ones because as we know that we have theta zero in the hypothesis so we have to insert one column so that we can multiply it with vector of theta. We are also going to randomly intialize value for theta's.

# Necessary Functions for Binary Logistic Regression
1. hypothesis()
2. sigmoid(h)
3. cost_function()
4. der_cost_function()
5. gradient_descent_function()
6. train_function(no_of_it_train,no_of_it_print_cost,lr=0.0001)
7. Predict(X)
8. get_weights()
9. printer()
10. Predict_Confidence(models_predictions)

# 1. hypothesis():

- This function is calculating hypothesis by taking dot product of X and theta vectors and then applying sigmoid on it.

# 2. sigmoid(h):

- This function take sigmoid of the given hypothesis.

# 3. cost_function():

- This function is calculating cost by taking mean of -((Y * np.log(hypothesis)) + ((1-Y) * np.log(1-hypothesis))).
  
# 4. der_cost_function():

- This function is calculating derivative of cost function by taking dot product of (hypothesis() - Y) and X. After that it take mean of this dot product.

# 5. gradient_descent_function():

- This function is calculating gradient descent meaning new value for theta by first taking derivative of cost function and then use this formula: new_theta = old_theta - learning rate * derivative of cost function.

# 6. train_function(no_of_it_train,no_of_it_print_cost,lr=0.0001):

- This function is used to train our regression model for no_of_it_train and print cost after no_of_it_print_cost. 

# 7.  Predict(X):

- This function is used to predict value on given X and returns it. 

# 8. get_weights():

- This function is used to return value of theta's.

# 9. printer():

- This function is used to print value of X, Y, theta's.

# 10. predict_confidence(models_predictions):

- It take model predictions and then use those to calculate the confidence but taking the max value from each model predictions and then give that class number to it.
- 
# Happy Coding:)
