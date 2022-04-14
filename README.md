# Credit_Risk_Analysis
In this project, we use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Using credit card data, we oversample the data using the RandomOverSampler and SMOTE algorithms and undersample the data using ClusterCentroids algorithm. Then, using the SMOTEEN algorithm we use a combination approach of over and under sampling. Finally, we compare the two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier to predict credit risk and make a recommendation on whether these models should be used to predict the credit risk.

## Overview of the analysis
Credit risk is an unbalanced classification problem, since good loans outnumber risky loans. Thus, it is important to employ different techniques to train and evaluate models with unbalanced classes. In this project, we use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. With the given credit card data, we oversample the data using the RandomOverSampler and SMOTE algorithms and undersample the data using ClusterCentroids algorithm. Then, we use a combinatorial approach of over and under sampling using the SMOTEENN algorithm. Finally, we compare two machine learning models that reduce bias to predict credit risk, called BalancedRandomForestClassifier and EasyEnsembleClassifier. Once these algorithms are complete, we can evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results
The data we were given contained 115,675 loan applications in Q1 from 2019. We used loan status to determine whether the application was considered low or high risk. We used all applications with a loan status of current to then separate into high and low risk bringing the total down to 68,817 applications with 99% of them considered as low risk and the other 1% high risk (see the count below).

![loan status risk](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/target-balance.png)

The data was split using the 75/25 method for training and testing so that we got a new count for low and high risk as seen below.

![test train balance](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/test-train-balance.png)

- Below we will show the balanced accuracy score, confusion matrix, and the imbalanced classification report with the precision and recall scores for each model
- Oversampling: classified 51,352 loans as high and low risk; from the two different models we get about 64%-65% balanced accuracy score

Naive random oversampling:

![naive oversampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/naive-oversampling.png)

- From above:
	- the low risk had a precision rate of 100% with a recall score of 68% and F1 score 81%
	- the high risk had a precision rate of 1% with a recall score of 62% and F1 score 2%

SMOTE oversampling:

![SMOTE oversampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/smote-oversampling.png)

- From above:
	- the low risk had a precision rate of 100% with a recall score of 66% and F1 score 79%
	- the high risk had a precision rate of 1% with a recall score of 63% and F1 score 2%

- Undersampling: classified 260 loans as high and low risk; balanced accuracy score of about 53%

![undersampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/undersampling.png)

- From above:
	- the low risk had a precision rate of 100% with a recall score of 45% and F1 score 62%
	- the high risk had a precision rate of 1% with a recall score of 61% and F1 score 1%

- Combination (over/under) sampling: classified 68460 high risk and 62011 low risk loans; balanced accuracy score of about 64%

![combo sampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/combination-sampling.png)

- From above:
	- the low risk had a precision rate of 100% with a recall score of 57% and F1 score 73%
	- the high risk had a precision rate of 1% with a recall score of 70% and F1 score 2%

- Ensemble algorithms

Balanced random forest classifier: balanced accuracy score of about 79%

![ensemble sampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/ensemble-sampling.png)

- From above:
	- the low risk had a precision rate of 100% with a recall score of 91% and F1 score 95%
	- the high risk had a precision rate of 4% with a recall score of 67% and F1 score 7%

Easy ensemble adaboost classifier: balanced accuracy score of about 93%

![easy ensemble sampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/images/easy-ensemble-sampling.png)

- From above:
	- the low risk had a precision rate of 100% with a recall score of 94% and F1 score 97%
	- the high risk had a precision rate of 7% with a recall score of 91% and F1 score 14%

## Summary
Overall, the results tell us that the best machine learning model is the easy ensemble Adaboost classifier based on the both the accuracy score as well as the precision rate/recall scores for both low and high risk. As you read above, all scores: the accuracy score, the precision rate and recall scores for low/high risk are the highest in this sampling compared to all other samplings (over, under, combination of over/under, balanced ensemble). We want a balanced accuracy score closest to 1 and a high precision and recall; however, a higher recall is more important than precision in this case because we would rather predict there is risk when there is not as opposed to predicting no risk when risk is present. It is possible to consider the F1 score if it is agreed that precision and sensitivity have the same importance. Thus, recommendation on which model to use is the easy ensemble adaboost classifier algorithm for the reasons we just listed and based on the scores presented in the results above. 


