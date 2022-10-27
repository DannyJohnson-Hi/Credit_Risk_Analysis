# Credit_Risk_Analysis

## Overview of the analysis: 

In this project I want to take a look at how all the factors in our loan_stats csv help predict whether someone is at a low or high risk status. One method that we used for this type of issue is creating a model and then evaluating and training the models that they create. For this project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first few models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

## Results: 

- Naive Random Oversampling results: Our balanced accuracy test it 64%, the precision for the high_risk has a very low positivity at 1% and the recall is 64%

![Images](https://github.com/DannyJohnson-Hi/Credit_Risk_Analysis/blob/main/images/oversample.png)


- SMOTE oversampling results: the accuracy score is 64.6%, the precision for the high_risk loans has a low positvity at 1% and recall is 63% overall

![Images](https://github.com/DannyJohnson-Hi/Credit_Risk_Analysis/blob/main/images/SMOTE.png)


- Undersampling results: balanced accuracy score is 51.5% overall, the precision is at 99% and the recall is 44%

![Images](https://github.com/DannyJohnson-Hi/Credit_Risk_Analysis/blob/main/images/undersampling.png)

- Combination(over and undersampling) results: balanced accuracy score is 61.4% the precision is 99% and the recall is 55% overall

![Images](https://github.com/DannyJohnson-Hi/Credit_Risk_Analysis/blob/main/images/combo.png)

- Balanced Random Forest Classifier results: the accuracy score is 78.9% the precision is 99% and the recall is 91%
- 
![Images](https://github.com/DannyJohnson-Hi/Credit_Risk_Analysis/blob/main/images/balanced.png)

- Easy Ensemble AdaBoost Classifier results: the accuracy score is 92.5% the precision is 99% and the recall is 94%
![Images](https://github.com/DannyJohnson-Hi/Credit_Risk_Analysis/blob/main/images/ensemble.png)

## Summary: 

In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are at the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
