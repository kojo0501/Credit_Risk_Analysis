# Credit_Risk_Analysis

## Overview of Analysis

### Purpose
The purpose is to evaluate machine learning models for predicting credit card risk. Credit risk is an unbalanced classification problem because the good loans outnumber the risky loans. Using a dataset from LendingClub, we evaluate the loan data with the following algorithms: RandomOverSampler, SMOTE, ClusterCentroids and SMOTEENN algorthms. Additionally, we'll compare two machine learning models to see how they predict risk: BalancedRandomForestClassifier and EasyEnsembleClassifier. These models will be evaluated on their performance predicting credit risk.

## Results

### Each Model with Scores for Balanced Accuracy, Precision, and Recall
* Naive Random Oversampling using RandomOverSampler
  * ![image](https://user-images.githubusercontent.com/24308495/151683570-d1e530b9-2426-4f39-96ed-a27f6ab1c215.png)
  * ![image](https://user-images.githubusercontent.com/24308495/151683580-c165128d-2a3a-4eaf-a2ba-297f03a9bcbe.png)
* SMOTE Oversampling using SMOTE
  * ![image](https://user-images.githubusercontent.com/24308495/151683631-9beba9a3-6daf-452a-a4ad-4bd5c5b7fff3.png)
  * ![image](https://user-images.githubusercontent.com/24308495/151683646-231b87e6-f3f1-4894-84fb-d2dd2e2e6a07.png)
* Undersampling using ClusterCentroids
  * ![image](https://user-images.githubusercontent.com/24308495/151685550-95c7c35e-9855-489d-8aca-bd2662330e7d.png)
  * ![image](https://user-images.githubusercontent.com/24308495/151685554-376fde5d-1114-41a8-91dd-b17ecf2b2625.png)
* Combination (Over and Under) Sampling using SMOTEENN
  * ![image](https://user-images.githubusercontent.com/24308495/151685566-af1916e6-21b3-4df5-b2d3-cdc8b841d733.png)
  * ![image](https://user-images.githubusercontent.com/24308495/151685568-5a327624-61f2-4673-8d39-a906af3af361.png)
* Balanced Random Forest Classifier using BalancedRandomForestClassifier
  * ![image](https://user-images.githubusercontent.com/24308495/151685587-804e32c0-7fc9-421c-a869-83546d940574.png)
  * ![image](https://user-images.githubusercontent.com/24308495/151685594-d3519fb4-2b73-4b4a-9d88-6d995c791446.png)
* Easy Ensemble AdaBoost Classifier using EasyEnsembleClassifier 
  * ![image](https://user-images.githubusercontent.com/24308495/151685637-5e6556f6-e312-4a5d-84a5-f1bc8323a251.png)
  * ![image](https://user-images.githubusercontent.com/24308495/151685645-b8dadfad-f1b0-497e-8832-9c6041358992.png)


## Summary

### Results

#### Precision
The precision for high risk loans was extremely low with all models. Random RandomOverSampler, SMOTE, ClusterCentroids and SMOTEENN algorthms all had a 0.01 score. The machine learning models had marginally better succes with BalancedRandomForestClassifier having a 0.03 score and the EasyEnsembleClassifier with a 0.09 score.

The precision for low risk loans was excellence across the board, with each one having a 1.00 score.

#### Recall
Recall scores varied drastically with all models. Random RandomOverSampler, SMOTE, ClusterCentroids and SMOTEENN, in general, faired poorer than the machine learning models. RandomOverSampler, SMOTE, ClusterCentroids and SMOTEENN had recall scores that for high risk loans that ranged between 0.61 and 0.78 and scores for low risk loans that ranged between 0.40 and 0.70.

The machine learning models generally faired better, with BalancedRandomForestClassifier having a recall score of 0.70 for high risk loans and a score of 0.87 for low risk loans. The EasyEnsembleClassifier performed the best with a recall score of 0.89 for high risk loans and a score of 0.95 for low risk loans.

### Recommendation
The best way to compare the models is by looking at the F1 scores. The best average F1 score was 0.97 from the EasyEnsembleClassifier model, with the BalancedRandomForestClassifier having an average F1 score of 0.93. The rest of the models average F1 scores ranged between 0.56 and 0.82.

The best model based on F1 score is the EasyEnsembleClassifier. The only issue with this model is the precision score of 0.09 for high risk loans. However, the recall score of 0.89 leads me to believe high risk loans won't be a signficant problem, despite the lack of precision.

