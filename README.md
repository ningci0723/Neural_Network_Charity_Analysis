# Credit Risk Analysis

## Overview

Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively



## Results

1. Data Preprocessing

* Variable that was considered as the target for my model: IS_SUCCESSFUL Column
* Variables that were considered features for my model: Every Column except for IS_SUCCESSFUL which is our target and the ones we will drop.
* Variable that were neither targets or features for the dataset: Columns that I dropeed are EIN, NAME because they will have little to no impact on our outcome.

2. Compiling, Training and Evaluating the Model
The number of neurons, layers, and activation functions I selected for my neural network model:

* For the neural network model I had 2 hidden layers. My first layer had 80 neurons, the second has 30 there is also an output layer. The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid."
![2 hidden layers](https://github.com/ningci0723/Neural_Network_Charity_Analysis/blob/main/Imgages/image%201.png)

The model was not able to reach the target 75%. The accuracy for my model was 51%.
![accuracy](https://github.com/ningci0723/Neural_Network_Charity_Analysis/blob/main/Imgages/image%202.png)

3. Removing features

When I remove "USE_CASE" Column. Rest of the model components stayed the same, however model accuracy went down to 53%.
![removing features](https://github.com/ningci0723/Neural_Network_Charity_Analysis/blob/main/Imgages/image%203.png)
![removing features accuracy](https://github.com/ningci0723/Neural_Network_Charity_Analysis/blob/main/Imgages/image%204.png)

4. Adding Additional neurons to hidden layers

When I added additional neurons to hidden layers and additional hidden layers are added. The accuracy was almost the same as this time it was 53%.
![adding hidden layers](https://github.com/ningci0723/Neural_Network_Charity_Analysis/blob/main/Imgages/image%205.png)

5. Changing activation function

When I chaged activation function to tanh. The accuracy was 53%.
![Changing activation function](https://github.com/ningci0723/Neural_Network_Charity_Analysis/blob/main/Imgages/image%206.png)


## Summary
The model ended up with the accuracy score of 53% after optimization. The initial neural network had a accuracy score of 51%. As we cannot achieve higher than 75% accuracy, we may need to further optimize our neural network by removing more features or simply adding more data to the dataset to increase accuracy.In addition, we could use the Random Forest classifiers to improve our accuracy.
