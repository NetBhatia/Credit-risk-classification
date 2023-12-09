Credit Risk Analysis Report:-

An overview of the analysis:
The purpose of this analysis is to create, train and evaluate the accuracy of a data model based on loan risk. The model will be trained to predict creditworthiness of potential borrowers from peer-to-peer lending services company.

For the purpose of creating a model, data was taken from lending_data csv file which carried the following information:
a. Loan Size
b. Interest Rate
c. Borrower Income
d. Debt to Income Ratio
e. Number of Accounts
f. Derogatory Marks
g. Total Debt
h. Loan Status

Loan Status was considered as target variable (y) while remaining inputs were considered as input factors (X). The model would need to predit variable y given the input factors X. A value of 0 in the “loan_status” column meanT that the loan is healthy. A value of 1 meant that the loan has a high risk of defaulting.

Using the train-test-split function data was split into 4 categories: X_train, X_test, y_train, y_test. Then using LogisticRegression function, a model was created. The data to be trained was fit into this model first. Then the X_test data was sent into this model for it to predict y values. Then the predicted y values were compared with y_test data using the 'balance accuracy score' and 'classification report' functions.

Then the data was resampled using the 'RandomOverSampler' function. The resampled data had equal number of data points. This was checked using 'Counter' function which was imported from collections. The model was recreated in a similar way as explained above using the LogisticRegression function. The random sampled data was trained and then tested to predict y values. The accuracy score was calculated for the predicted values and actual values, using the 'balance accuracy score' and 'classification report' functions.

The results: Accuracy score, the precision score, and recall score of the machine learning model:

Machine Learning Model 1:

The balanced accuracy score of the model is: 0.9520479254722232

Description of Model 1 Accuracy, Precision, and Recall scores.

                precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

The logistic regression model was at 95% accuracy rate i.e., given the X features it is able to predict the loan status at an accuracy rate of 95% which indicates it is a good performance model.

Machine Learning Model 2 (created on randomly sampled data):

The balanced accuracy score of the model is: 0.9945026387334079

Description of Model 2 Accuracy, Precision, and Recall scores.

              precision    recall  f1-score   support

           0       0.99      0.99      0.99     75036
           1       0.99      0.99      0.99     75036

    accuracy                           0.99    150072
   macro avg       0.99      0.99      0.99    150072
weighted avg       0.99      0.99      0.99    150072

The logistic regression model was at 99% accuracy rate i.e., given the X features it is able to predict the loan status at an accuracy rate of 99% which indicates it is a very good performance model.

A summary:
I recommend using this model to predict the creditworthiness of borrowers, because it has over 95% accuracy in predicting if the loan will be repaid in full. The model can be embedded into business structure for day to day use and right decision making to support customers by providing them necessary financing and helping them support their day to day working capital needs, at the same time supporting the company's earnings within a reasonable risk level.