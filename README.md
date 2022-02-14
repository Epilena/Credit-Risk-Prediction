# Credit-Risk-Prediction
### Supervised Machine Learning, Credit Analysis

## Introduction
The purpose of this project is to build a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not.  LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market.  Previous loan data is offered from LendingClub through an API.

## Methods
The project utilized LendingClub loan data from 2019 and 2020Q1.  The data was used to create machine learning models to classify the risk level of given loans.  The two models utilized are Logistic Regression and Random Forest Classifer.  
Data was preprocessed:
  1. training data set created from 2019 entire year data
  2. pd.get_dummies() utilized on training data to convert categorical data to numeric columns
  3. testing data set created from Q1 2020 loan data
  4. column created with dummy values (one additional column in training set not in testing set)

## Analysis
The data has been undersampled to give an even number of high risk and low risk loans.  This was done because only 2.2% of the loans in the orignial dataset were categorized as high risk.  Because the data is imbalanced undersampling was utilized for a more accurate model.  

The models were used on data that had not been scaled.  Data was then scaled and models were rerun.  

![pic notebook](https://user-images.githubusercontent.com/88807979/153782310-42d87872-b343-475a-ad6e-b592c1674dce.png)

## Discussion/ Conclusion

I predicted the Logistic Regression model to perform better when compared to the Random Forest Classifier.  Models perfromed on the unscaled data demonstrated the Random Forest Classifer performed better as a model, with a score of 0.635.  The scaled data reduced the score of both models, however the Logisitc Regression model performed better than the Random Forest Classifer model.  The scores were 0.549 and  0.515 respectively.  I expected improvement in both models with scaled data which was not the outcome.  
The final best model for the data is Random Forest Classifer on data that has not been scaled. 
