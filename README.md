# Neural Network Charity Analysis

## Purpose

The purpose of this notebook is to explore using a neural network to help predict if certain charities are worth funding.

## Data Preprocessing

- What variable(s) are considered the target(s) for your model?
  - I used the `IS_SUCCESSFUL` column as the target column.
- What variable(s) are considered to be the features for your model?
  - All other columns were considered the features.
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - The only features removed were the `EIN` and `NAME` columns as these are not usable features and are unique, thus not very good for modeling.

## Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - I used two hidden layers, one with 6 neurons and the second with 4. Both layers used RELU activation functions. The neural net was then trained for 100 epochs using binary crossentrop as the loss metric and the ADAM optimizer.
- Were you able to achieve the target model performance?
  - I was unable to acheive 75% accuracy unfortunately, I was only able to acheive 72.7% accuracy on the test set.
- What steps did you take to try and increase model performance?
  - To begin with, I tried training the saved neural network 100 epochs more. After this, I tried adding a hidden layer. Both of these strategies improved the performance very little, at most an increase in accuracy of 1%. Besides these two, I also tried binning the categorical columns of `APPLICATION_TYPE` and `CLASSIFICATION` in slightly more bins. This also did not greatly improve the performance of the neural network. I also experimented with changing the activation functions for the hidden layers, but again this did not offer a significant improvement.

## Summary

In summary, the last neural network created, with (6, 8, 6) neurons with `tanh` activation functions was best at predicting successful charity organizations. The dataset does need some preprocessing of the `APPLICATION_TYPE` and `CLASSIFICATION` columns by binning, but not by an aggresive amount.
