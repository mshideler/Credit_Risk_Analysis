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

- The balanced accuracy for the model is 66.2%, which isn't too bad.  Balanced accuracy is used here because to account for the imbalance between high credit card risk and low credit card risk.  It's the arithmetic mean of recall (true positive rate) and specificity (true negative rate).
- Precision ("pre" column in the imbalanced classification report) is very high at 99%.
- Recall ("rec" column in the imbalanced classification report) is okay at 60%.
- The F1 score in the imbalanced classificaton looks good at 75%.
- While the above metrics look good, they are misleading when taking into account that the precision and F1 score for high-risk credit card applicants (group 0 in the imbalanced classification report) are practically 0.  This means this model isn't very precise when determining if an applicant is high-risk but great at predicting low-risk applicants.

### SMOTE Oversampling

Balanced Accuracy

![SMOTE Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smote_acc.PNG)

Imbalanced Classification Report

![SMOTE ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smote_icr.PNG)

- The balanced accuracy for the model is 65.7%, which isn't too bad.
- Precision is very high at 99%.
- Recall is pretty good at 70%.
- The F1 score looks really good at 82%.
- While the above metrics look good, again they are misleading when taking into account that the precision and F1 score for high-risk applicants are practically 0, meaning this model isn't very precise when determining if an applicant is high-risk but great at predicting low-risk applicants.

### Cluster Centroids (Undersampling)

Balanced Accuracy

![CC Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/cc_acc.PNG)

Imbalanced Classification Report

![CC ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/cc_icr.PNG)

- The balanced accuracy for the model is 54%, which isn't very good.
- Precision is very high at 99%.
- Recall is low at 40%.
- The F1 score is okay at 56%.
- For the most part, except precision, the above metrics are lower than those for the oversampling algorithms.  This doesn't appear to be a very good model to use to predict high-risk applicants, especially when again the precision and F1 score for high-risk applicants are practically 0 for this group.

### SMOTEENN Combination Under- and Oversampling

Balanced Accuracy

![SMOTEENN Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smoteenn_acc.PNG)

Imbalanced Classification Report

![SMOTEENN ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/smoteenn_icr.PNG)

- The balanced accuracy for the model is 67.8%, which isn't bad.
- Precision is very high at 99%.
- Recall is okay at 57%.
- The F1 score is pretty good at 72%%.
- While the above metrics make this model look ok at predicting high-risk applicants, the precision and F1 score for high-risk applicants are still really low for this group.

### Balanced Random Forest Classifier

Balanced Accuracy

![BFR Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/brf_acc.PNG)

Imbalanced Classification Report

![BFR ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/bfr_icr.PNG)

- The balanced accuracy for the model is 78.8%, which very good.
- Precision is very high at 99%.
- Recall is very high at 87%.
- The F1 score is great at 93%.
- The above metrics make this model look successful when predicting high-risk applicants; however, the precision and F1 score for high-risk applicants are still really low for the high-risk group.

### Easy Ensemble AdaBoost Classifier

Balanced Accuracy

![EEC Balanced Accuracy](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/eec_acc.PNG)

Imbalanced Classification Report

![EEC ICR](https://github.com/mshideler/Credit_Risk_Analysis/blob/main/Resources/eec_icr.PNG)

- The balanced accuracy for the model is 93.2%, which is great.
- Precision is very high at 99%.
- Recall is very high at 94%.
- The F1 score is great at 97%.
- The above metrics make this model look the most successful when predicting high-risk applicants; however, the precision and F1 score for high-risk applicants are still really low for the high-risk group.

## Summary

Of all the algorithms tested, the Easy Ensemble AdaBoost Classifier appears to be the most successful model at predicting credit card risk; however, all models did poorly in precision and the F1 score specifically for those labeled high-risk.  This means no model here is successful at predicting high-risk applicants as the tendency is label everyone as low-risk, thus causing high risk for anyone issuing credit cards using these models.