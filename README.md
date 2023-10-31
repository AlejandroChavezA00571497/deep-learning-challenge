# deep-learning-challenge
Module 21 Challenge for the Tec de Monterrey Data Analysis Bootcamp, Introduction to Neural Networks

Jupyter notebook files that take in data from a remote CSV and perform Neural Network analysis on them in order to create a predictive model, in this case used to aid in the selection of applicants for funding in a nonprofit foundation

Main_Deep_Learning.ipynb is the main file, it uses data related to a nonprofit fundation’s project funding in order to build a neural network that outputs a binary classification, regarding whether it will be successful or not.

The basic processes for the building of this model are:
- Data Preprocessing by removing non-necessary columns and binning data, as well as converting categorical data to numeric.
- Splitting into features and arrays, as well as scaling features.
- Compiling the model, establishing the structure of layers and neurons, as well as activation functions, loss functions, optimizers and metrics.
- Fitting the model to training
- Evaluating the model’s accuracy and loss.
- Exporting the model into an .h5 file


AlphabetSoupCharity.h5 is the model’s file output.

AlphabetSoupCharity_Optimization.ipynb is the second file, which performs most of the same processes as Main_Deep_Learning.ipynb but also tries to optimise the model’s performance through changing the binning of features, optimising through Keras Tuner and using Model Ensembling to achieve a higher accuracy value.

All files exist in the main directory, as well as the README, a detailed report on the project, and the untitled_project directory, which contains json files for the Keras Tuner optimization method.

Contributions:
- Data Analysis Bootcamp Classes
- https://scikit-learn.org/stable/modules/ensemble.html
- https://playground.tensorflow.org
- https://www.tensorflow.org/api_docs/python/tf/keras/optimizers/Adam
- https://www.tensorflow.org/model_optimization


