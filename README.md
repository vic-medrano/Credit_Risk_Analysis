# Credit_Risk_Analysis
## Overview
The purpose of this analysis was to examine a variety of different techniques to evaluate data with unbalanced classes such as credit risk. Machine learning methods such as the BalancedRandomForestClassifier and EasyEnsembleClassifer were used once the data had been over and under-sampled to predict credit risk.
## Results
### Random OverSampling
![image](https://user-images.githubusercontent.com/102090016/182063812-6d0f9945-88d1-4cf6-9140-f2efb480a0ab.png)
When over-sampling data we can see that the balanced accuracy score is 65%
To further break this number down we can analyze the confusion matrix and look at the precision and recall scores of this model 

![image](https://user-images.githubusercontent.com/102090016/182064044-5ade56dc-0ef9-4d3e-84f4-80db86fac07e.png)
![image](https://user-images.githubusercontent.com/102090016/182064078-41adebe7-0a75-4357-87cb-81d9e0b80754.png)
These images show that the precision for high_risk is about 1% with a 62% recall. Leaving us with an F1 of 2%. When looking at the low risk population, the precision is close to 100% and the recall is 65%.
### SMOTE Model
### ClusterCentroids model
### SMOTEENN Model
### BalancedRandomForestClassifier Model
Easy EnsembleClassifier Model
## Summary
