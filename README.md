# Credit_Risk_Analysis
In this project, we use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Using credit card data, we oversample the data using the RandomOverSampler and SMOTE algorithms and undersample the data using ClusterCentroids algorithm. Then, using the SMOTEEN algorithm we use a combination approach of over and under sampling. Finally, we compare the two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier to predict credit risk and make a recommendation on whether these models should be used to predict the credit risk.

## Overview of the analysis
Credit risk is an unbalanced classification problem, since good loans outnumber risky loans. Thus, it is important to employ different techniques to train and evaluate models with unbalanced classes. In this project, we use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. With the given credit card data, we oversample the data using the RandomOverSampler and SMOTE algorithms and undersample the data using ClusterCentroids algorithm. Then, we use a combinatorial approach of over and under sampling using the SMOTEENN algorithm. Finally, we compare two machine learning models that reduce bias to predict credit risk, called BalancedRandomForestClassifier and EasyEnsembleClassifier. Once these algorithms are complete, we can evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results
- Below we will show the balanced accuracy score, confusion matrix, and the imbalanced classification report with the precision and recall scores for each model
- Oversampling
	- Naive random oversampling:

![naive oversampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/naive-oversampling.png)

	- SMOTE oversampling:

![SMOTE oversampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/smote-oversampling.png)

- Undersampling

![undersampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/undersampling.png)

- Combination (over/under) sampling

![combo sampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/combination-sampling.png)

- Ensemble algorithms
	- Balanced random forest classifier

![ensemble sampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/ensemble-sampling.png)

	- Easy ensemble adaboost classifier

![easy ensemble sampling](https://github.com/kmaluccio/Credit_Risk_Analysis/blob/main/easy-ensemble-sampling.png)


## Summary
Overall, the results tell us that the best machine learning model is HERE based on the OUTCOME HERE. The recommendation(s) on which model to use includes THIS because REASON. 


