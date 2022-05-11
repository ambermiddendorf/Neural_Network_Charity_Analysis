# Neural Network Charity Analysis
Module 19 - Deep Machine Learning

## Overview of the loan prediction risk analysis:
Given the data set, the goal is to determine which loan applications will be "successful" or use their money effectively. In preparing the data for the neural network, Application Type and Classification fields needed to be bucketed. I made an other bucket for those with less than 700 results for each of those fields. I also narrowed the options for Income Amount, grouping all those with more than $1 million in income, this was done in the process of trying to improve accuracy of the model. In the same manner, I grouped the Affiliation responses that weren't "Independent" or " Company Sponsored" into the "Other" group. The data was onehotencoded for all the object fields and then StandardScaler was used to normalize the data.

## Results:

### Data Preprocessing
* The target field for the model was "IS_SUCCESSFUL", to decide if the loans were used effectively.
* The features of our model included: Application_Type, Affiliation, Classification, Use Case, Organization type, Income Amount, and Ask Amount.
* EIN, Name, Status (since so few were inactive), and Special Considerations (since so few had any) were removed from the input data.

### Compiling, Training, and Evaluating the Model
* My final model had 80 neurons in the first layer and 40 in the second layer. I used the relu activation function for the first two layers and the sigmoid function for the output layer. I did try other activation functions including tanh, sigmoid, and softmax for the first two layers, but did not find them to increase the accuracy. 
* I did not get to .75 accuracy. My final model gave an accuracy of .733. 
* To try to reach the .75 accuracy, I tried many different neurons and different activation functions as well as adding and removing layers. I took out the input features "Special Considerations" and "Status", also without marked improvement. I further bucketed Affiliation and Income Amount in another attempt to increas accuracy, but again it did not improve results.

## Summary:

There is a summary of the results (2 pt)
There is a recommendation on using a different model to solve the classification problem, and justification (3 pt)
