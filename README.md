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

Then, I split the data into separate training and testing datasets by employing the `train_test_split` function.

## Create a Logistic Regression Model with the Original Data
Next, I fit a logistic regression model by using the training data (`X-train` and `y_train`). I saved the predictions for the testing data lables by using the testing feature data(`X_test`) and the fitted model. To evaluate the model's performance I checked the following:
- Calculate the accuracy score of the model.
- Generate a confusion matrix.
- Print the classification report
<img width="500" src="https://github.com/nancygmz/credit-risk-classification/blob/main/Credit_Risk/Resources/model%201.png">

## Predict a Logistic Regression Model with Resampled Training Data
Next, I imported the RandomOverSampler module from imblearn and fit it to the original training dataset. I then fit the sampleted data to logistic regression model. To evaluate the sampled model's performance I checked the following:

- Calculate the accuracy score of the model.
- Generate a confusion matrix.
- Print the classification report.
<img width "700" src="https://github.com/nancygmz/credit-risk-classification/blob/main/Credit_Risk/Resources/model%202.png">

## Summary
In summary, Model 2 shows better performance in terms of precision and recall for high-risk loans, outperforming Model 1. However, it demonstrates slightly lower precision and recall for healthy loans. Nevertheless, considering the higher accuracy rate for high-risk loans and the overall trend, Model 2 is a more reliable choice for credit risk prediction.
