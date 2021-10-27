# Neural_Network_Charity_Analysis

## Overview of the analysis
USing knowledge of machine learning and neural networks, we used the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization. 
This project consists of the following deliverables:

- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model
- Deliverable 3: Optimize the Model

## Results: Using bulleted lists and images to support your answers, address the following questions.

Data Preprocessing
What variable(s) are considered the target(s) for your model?
IS_SUCCESSFUL

What variable(s) are considered to be the features for your model?
The features in this model are all other columns:

ORGANIZATION
STATUS
INCOME_AMT
SPECIAL_CONSIDERATIONS
ASK_AMT
APPLICATION_TYPE
AFFILIATION
CLASSIFICATION
USE_CASE


What variable(s) are neither targets nor features, and should be removed from the input data?
NAME and EIN.

Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
- 2 hidden layers
- first layer - 80 neurons
- second layer - 30 neurons

![image](https://user-images.githubusercontent.com/84201614/138983867-70aa8770-748e-4ba6-85d0-fea9f4ffa177.png)


Were you able to achieve the target model performance?

- Attempt 1:
    - Removed 'USE_CASE' column. The model remained close to the same. There was a slight increase in accuracy
    - ![image](https://user-images.githubusercontent.com/84201614/138984586-7501e5f2-24ee-4e88-8acd-90f4bfef063a.png)

- Attempt 2
    - Additional neurons were added and the accuracy went down to 53%
    - ![image](https://user-images.githubusercontent.com/84201614/138984898-74d7d194-0bd7-4834-bc48-040015ffb202.png)

- Attempt 3
    - Changed activation function of output layer from "sigmoid" to "tanh." The accuracy of the model went down to 46%
    - ![image](https://user-images.githubusercontent.com/84201614/138985118-4b2d1a04-2f5c-4eec-8eb4-813c7668dd22.png)

The model did not acheive the target of 75% accuracy. 


## Summary:
The model ended up with 46% accuracy after optimization as opposed to the starting accuracy of the mdoel at 69%. The model seems to have been overfitted and therefore causing a derease in accuracy. Random Forest Classifiers could have been used to represent a more in depth group of decision trees to create more accurate classifications.
