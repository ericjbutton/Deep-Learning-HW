# Deep-Learning-HW
Unit 21 Homework: Charity Funding Predictor

- Steps 1 & 2 found in AlphabetSoupCharity.ipynb
- Step 3 found in AlphabetSoupCharity_Optimization.ipynb

# Step 4: Write a Report on the Neural Network Model
## Overview
The objective is to compile, train, and evaluate a neural network model for the purpose of predicting whether applicant will be successful if funded by Alphabet Soup.

## Results
Data Preprocessing
- The target is the IS_SUCCESSFUL column to determine if a venture is succesful after recieving funding.
- The features for the model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
- NAME and EIN are neither targets nor features and should be removed from the model because they are simply identification columns.
Compiling, Training, and Evaluating the Model
- The initial model was built with 1 neuron, 1 layer, a relu activation input function, and a sigmoid activation output function for simplicity to get an initial look at how the model performs as a basic neural network. This produced 72% model accuracy, which was close but did not meet target performance of 75% model accuracy.
- Attempts to optimize performance:
  - Adding a hidden layer to consider more interactions between variables. This reduced model accuracy to 70%
  - Increasing the number of neurons from 1 to 10 for the both hidden layers. This reduced model accuracy to 48%.
  - Changed activation input function to Leaky Relu. This reduced model accuracy to 50%.
  
## Summary
The first attempt at creating the model produced the highest accuracy at 72%, and attempts at optimization only made the model less accurate. For future attempts to optimize, reducing/increasing the number of epochs could increase accuracy as the model may be under/overfitted. Additionally, reducing the number of columns in the preprocessing stage may have led to a more accurate model as well. An unsupervised learning model may solve this classification problem with applied dimensionality reduction to limit the amount of potential noise in this dataset. Finally, using keras-tuner to optimize hyperparameters could have increased model accuracy.
