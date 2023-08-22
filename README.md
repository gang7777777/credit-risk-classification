# credit-risk-classification

Machine learning techniques, specifically supervised learning techniques were used to analyze the dataset of lending acitivty to build a model that can identify the creditworthiness of a borrower.

Different factors were considered in the analysis. This includes:
 - loan size
 - interest rate
 - borrower's income
 - debt to income ratio
 - number of accounts
 - any derogatoty marks against the borrower
 - total debt

The dataset composing of 77,536 data points was split into training and testing subsets. The original training set was used to build a logistic regression model for the purpose of classify whether the loan would have a low- or high- risk result.

The original testing set then was used to predict the outcome using the model extracted from the first dataset. 

The training dataset was then resampled using the Random Over Sampler module to confirm that the labels would have an equal number of data points. 

The resampled data was then used to build a new logistic regression model which is to be used to test the testing set to predict outcomes.

The results are as follows:

Logistic Regression Model (original training set):
- Precision: 100% for the low-risk loans and 84% for the high-risk loans
- Accuracy: 99%
- Recall: 100% for low-risk loans and 89% for high-risk loans

Logistic Regression Model (random over sampler training set):
- Precision: 100% for healthy loans and 87% for high-risk loans
- Accuracy: 100% 
- Recall: 100% for healthy loans and 100% for high-risk loans

Summary:

The logistic regression model using the random over sampler training set is less likely to predict false negative results. However, based on the confusion matrices, this model predicted more false positives.

The logistic regression model using the original set had slightly more true positives. However, this model also predicted more false predictions.

If the goal is to determine the accuracy of the predictions, both models can be used. But if the goal is to determine the likelihood of high-risk loans, it is less likely to use both models because of it's lower than 90% precision range. The logistic regression with the random over sample set would be the most logical choice to be used based on high accuracy and high recall.