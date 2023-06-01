# credit-risk-classification
## Overview of the Analysis
Using historical lending activity dataset from a peer-to-peer lending services company, I built a model that can identify the creditworthiness of borrowers. This challenge included the following steps:
  * Split the Data into Training and Testing Sets

  * Create a Logistic Regression Model with the Original Data

  * Predict a Logistic Regression Model with Resampled Training Data

  * Write a Credit Risk Analysis Report


## Split the Data into Training and Testing Sets
I first read in the `lending_data.csv`file from the Resources folder and into a Pandas DataFrame. Then, I extracted the "loan_status" column to create the labels set (y),and the remaining columns to create features (X) dataframe. 

In the "loan_status" column, a value of 0 signifies a healthy loan, while a value of 1 indicates a loan with a high risk of default.

After reviewing the data, I divided it into separate training and testing datasets by employing the `train_test_split` function.
