# Credit_Risk_Analysis

## Overview

The purpose of this analysis is to evaluate how well supervised machine learning predicts credit card risk.  We specifically use analyze the performance of the following models:  RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier and EasyEnsembleClassifier.

## Results

The dataset used in this analysis was loan information from Q1 2019.  This dataset included information such as loan amount, interest rate, home ownership, annual income, bankruptcies, hardship and debt settlement among others.  For consistency in testing, a random state of 1 was used in each algorithm.

### Random Oversampling

Balanced Accuracy
![ROS Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/ros_acc.PNG)

Imbalanced Classification Report
![ROS ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/ros_icr.png)

### SMOTE Oversampling

Balanced Accuracy
![SMOTE Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smote_acc.PNG)

Imbalanced Classification Report
![SMOTE ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smote_icr.PNG)

### Cluster Centroids (Undersampling)

Balanced Accuracy
![CC Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/cc_acc.PNG)

Imbalanced Classification Report
![CC ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/cc_icr.PNG)

### SMOTEENN Combination Sampling

Balanced Accuracy
![SMOTEENN Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smoteenn_acc.PNG)

Imbalanced Classification Report
![SMOTEENN ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smoteenn_icr.PNG)

### Balanced Random Forest Classifier

Balanced Accuracy
![BFR Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/brf_acc.PNG)

Imbalanced Classification Report
![BFR ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/bfr_icr.PNG)

### Easy Ensemble AdaBoost Classifier

Balanced Accuracy
![EEC Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/eec_acc.PNG)

### Imbalanced Classification Report
![EEC ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/eec_icr.PNG)

## Summary