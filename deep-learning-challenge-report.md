#  Deep Learning Challenge Report

### Overview

This project had the purpose of creating a neural network model capable of predicting the success of a campaign funded by the nonprofit foundation AlphabetSoup, based on a series of features. The features, as well as labels for the target data where given in a CSV file with more than 34,000 projects’ information, distributed into the following categories:


- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

With this data a model was created, with the following general steps being followed:

- Data Preprocessing by removing non-necessary columns and binning data, as well as converting categorical data to numeric.
- Splitting into features and arrays, as well as scaling features.
- Compiling the model, establishing the structure of layers and neurons, as well as activation functions, loss functions, optimizers and metrics.
- Fitting the model to training
- Evaluating the model’s accuracy and loss.
- Exporting the model into an .h5 file

It’s important to note that the model was further optimised through the usage of different binning structures, Keras Tuner, and model ensembling.



### Results

##### Data Preprocessing:

- The target variable for our model was the IS_SUCCESSFUL column, which stablished whether the money for the project had been used effectively.

- The features for our model were: application type, affiliation, classification, use case, organization, status, income amount, special considerations and ask amount.

- The variables that were removed from our data, because they were neither features nor targets were the EIN and Name, identification columns for each project.


#####  Compiling, Training, and Evaluating the Model

- In the first, non-optimized model, 3 layers with 10 neurons each were selected, as an starting point, all with relu activation functions and an output layer with a sigmoid function, a setup considered good for initial testing, as well as compiling with a binary_crossentropy loss function, adam optimizer and 50 epochs.

- The first accuracy score was around 72.95%, below the 75% optimization score.

- Steps taken to increase the model’s performance were the iteration of the model with increasing numbers of functions, layers, trying many activation functions as well as loss functions and optimization models, eventually landing on trying Keras Tuner to get some recommendations for our model’s architecture, and using Model Ensembling to get to a total ensemble accuracy score of 81.44% with a RandomForestClassifier structure.


##### Summary

Overall, after optimization methods and landing on Model Ensembling, the accuracy was made to be 81.44%, above our goal of 75%, however, further testing to establish an optimal number of layers and neurons, as well as a specific configuration of activation and loss functions as well as optimization models could take the accuracy score even further, as well as applying data regularization techniques.
