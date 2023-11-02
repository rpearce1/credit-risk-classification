# credit-risk-classification

## Overview of the Analysis

In this analysis, we wanted to create a model to predict if a loan was healthy or high-risk using a data set of 75,036 healthy loans and 2,500 high-risk loans. Each loan included information on loan size, interest rate, borrower income, number of accounts, derogatory marks, borrower to income ratio, and total debt. From these different factors we can have a good picture of the loan itself and the borrower’s financial state.

A logistic regression model was initially trained and tested on the original data set. We used sklearn in Python for fitting the model and splitting the data set into a larger training set and smaller test set. We fit the model again using a randomly oversampled data set, using imblearn, to give us an even ratio of healthy to high-risk loans, 56,271 loans for each.The analysis was also performed again with only loan size, borrower income, and total debt as predictors.

## Results

### Machine Learning Model 1:
  
* Balanced Accuracy: 95%
* Precision for healthy loans: 100%
* Precision for high-risk loans: 85%
* Recall for healthy loans: 99%
* Recall for high-risk loans: 91%

### Machine Learning Model 2:
  
* Balanced Accuracy: 99%
* Precision for healthy loans: 100%
* Precision for high-risk loans: 84%
* Recall for healthy loans: 99%
* Recall for high-risk loans: 99%

## Summary

Both models were very good at predicting loan type, especially healthy loans, but with random oversampling, we were able to get an improved recall for high-risk loans. Precision for high-risk loans is the only remaining weakness, although 84% is still good, especially in the interest of the lender, where it won’t matter as much if a small number of healthy loans are classified as high-risk. The reduced number of predictors yielded the same result, demonstrating that we really only need loan size, borrower income, and total debt to accurately predict loan type.
