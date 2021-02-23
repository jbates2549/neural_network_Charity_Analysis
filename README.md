# neural_network_Charity_Analysis

## Overview
In this analysis we use neural network learning to analyze a charity campaign to determine the factors that lead to successful outcomes.

We begin by loading a data file with charity donation data.  We remove unnnecessary columns and bin data for efficient machine processing.  Then we use One hot Encoder to fit the data for the analysis models.  Finally we define our deep learning model and evaluate the data.  The goal is to have a predictive accuracy over 75%.

## Results

### Data Preprocessing

* Target variables - The Is_SUCCESSFUL variable is our target variable.  The model will attempt to predict the outcome of this variable.
* Feature variables - Application Type, Income Amount and Classification variables are feature variables, key variables to predict the outcome of the target variable.
* Variables removed - We removed the EIN and NAME variables as they do not have predictive relevence.

### Compiling Training and Evaluating the Model

* First Pass Model
In this model we used 2 hidden layers with 8 nodes in the first layer and 5 nodes in the second layer.  Both layers used the Relu activation model.  THe output layer used the Sigmoid activation model.  As shown below, the model produced an accuracy of 55.7 % with 100 epochs.

![image_name](https://github.com/jbates2549/neural_network_Charity_Analysis/blob/main/Resources/first_pass_model.PNG)


* 1st Optimization

In this optimization the Affiliation and Special Considerations columns are removed as they do not appear to contribute to the accuracy of the model.
This model gave us an accuracy score of 58.7.

![image_name](https://github.com/jbates2549/neural_network_Charity_Analysis/blob/main/Resources/optimization_1.PNG)


* 2nd Optimization

For this optimization we increased the hidden layers to 3 with 10 nodes in layer 1, 5 nodes in layer 2 and 2 nodes in layer 3.  We used the Relu activation model for each hidden layer and Sigmoid for the output layer.  Interestingly the added layers and nodes actually decreased the accuracy of the model to  52.9%.

![image_name](https://github.com/jbates2549/neural_network_Charity_Analysis/blob/main/Resources/optimization_2.PNG)


* 3rd Optimization
For this optimization we return to 2 hidden layers with 8 nodes in layer 1 and 5 nodes in layer 2.  The first layer uses Relu activation while the second layer uses Leaky Relu.  We, again, use Sigmoid for the output layer.  This model gives us an accuracy of 56.8%.

![image_name](https://github.com/jbates2549/neural_network_Charity_Analysis/blob/main/Resources/optimization_3.PNG)


## Summary

In addition to the optimization models presented, we experimented with various combinations of activation models, layers and nodes.  We also attemped to increase the number of epochs to 500.  Despite these efforts, we were not able to achieve the desired accuracy of 75%.  

For further analysis we recommend an additional analysis using the Random Forest classifier to compare the results to the deep learning model.





