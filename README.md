# Neural_Network_Charity_Analysis

## Overview

This analysis uses deep neural networks to create a binary classifier that can predict whether charities applying for funding from Alphabet Soup will be successful. It employs a dataset with more than 34,000 organizations which have previously received funding from Alphabet Soup. The dataset includes the following variables for each charity:

EIN and NAME — Identification columns  
APPLICATION_TYPE* — Alphabet Soup application type  
AFFILIATION* — Affiliated sector of industry  
CLASSIFICATION* — Government organization classification  
USE_CASE* — Use case for funding  
ORGANIZATION* — Organization type  
STATUS* — Active status  
INCOME_AMT* — Income classification  
SPECIAL_CONSIDERATIONS* — Special consideration for application  
ASK_AMT* — Funding amount requested  
IS_SUCCESSFUL — Was the money used effectively  


## Results

The analysis employed TensorFlow to build deep neural network models with nine features (indicated above with asterisks). The "IS_SUCCESSFUL" variable was the target of these models. The two identification variables ("EIN" and "NAME") were removed from the input data.

Four model runs were conducted, with the following run parameters:

1) AlphabetSoupCharity
APPLICATION_TYPE binned into 9 values.
CLASSIFICATION binned into 6 values.
First hidden layer with 80 nodes, RELU activation function.
Second hidden layer with 30 nodes, RELU activation function.
Output layer used SIGMOID activation function.
Loss: 0.556
Accuracy: 0.727

2) AlphabetSoupCharity_Optimization_1
APPLICATION_TYPE binned into 9 values
CLASSIFICATION and STATUS variables deleted.
First hidden layer with 50 nodes, RELU activation function.
Second hidden layer with 20 nodes, RELU activation function.
Output layer used SIGMOID activation function.
Loss: 0.572
Accuracy: 0.719

3) AlphabetSoupCharity_Optimization_2
APPLICATION_TYPE binned into 13 values.
CLASSIFICATION binned into 13 values.
First hidden layer with 100 nodes, RELU activation function.
Second hidden layer with 50 nodes, RELU activation function.
Output layer used SIGMOID activation function.
Loss: 0.556
Accuracy: 0.726

4) AlphabetSoupCharity_Optimization_3
APPLICATION_TYPE binned into 13 values.
CLASSIFICATION binned into 17 values.
First hidden layer with 190 nodes, RELU activation function.
Second hidden layer with 50 nodes, RELU activation function.
Third hidden layer with 10 nodes, RELU activation function.
Output layer used SIGMOID activation function.
Loss: 0.568
Accuracy: 0.728

## Summary

I was unable to raise the accuracy of the model to the target value of 0.75.
This indicates that changes in variable binning, variable selection, # of neurons, and the addition of a third hidden layer created no meaningful improvements in model performance. Future analysis should move on to testing model performance with new combinations of activation functions. 


