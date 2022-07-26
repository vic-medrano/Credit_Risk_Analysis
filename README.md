# Credit_Risk_Analysis
## Overview
The purpose of this analysis was to examine a variety of different techniques to evaluate data with unbalanced classes such as credit risk. Machine learning methods such as the BalancedRandomForestClassifier and EasyEnsembleClassifer were used once the data had been over and under-sampled to predict credit risk.
## Results
### Random OverSampling
![image](https://user-images.githubusercontent.com/102090016/182063812-6d0f9945-88d1-4cf6-9140-f2efb480a0ab.png)
![image](https://user-images.githubusercontent.com/102090016/182064044-5ade56dc-0ef9-4d3e-84f4-80db86fac07e.png)
![image](https://user-images.githubusercontent.com/102090016/182064078-41adebe7-0a75-4357-87cb-81d9e0b80754.png)
When over-sampling data we can see that the balanced accuracy score is 65%
To further break this number down we can analyze the confusion matrix and look at the precision and recall scores of this model 
These images show that the precision for high_risk is about 1% with a 62% recall. Leaving us with an F1 of 2%. When looking at the low risk population, the precision is close to 100% and the recall is 65%.
### SMOTE Model
![image](https://user-images.githubusercontent.com/102090016/182064875-15ecb53f-9f6c-4746-8eb9-ca483dc27a66.png)
![image](https://user-images.githubusercontent.com/102090016/182064926-da154bbf-3daa-4f43-84e9-4d70c73317f1.png)
![image](https://user-images.githubusercontent.com/102090016/182064965-94fb7103-b629-4c22-8344-f2aaff11624b.png)
As with the previous model, the balanced accuracy score of 65% is not quite at an acceptable level. From the third image we can see that the high risk precision is around 1% and the recall is 62% which equates to an F1 of 2%. We also know that the high risk population had a much smaller sample size than the low_risk population, the size of the low risk population has an increased precision of 100% and recall of 65%
### ClusterCentroids model
![image](https://user-images.githubusercontent.com/102090016/182065035-9c124d34-3be4-49a0-a9d6-326cb169d66f.png)
![image](https://user-images.githubusercontent.com/102090016/182065083-c144d6cd-1964-4c35-ba95-49a569b9aa86.png)
![image](https://user-images.githubusercontent.com/102090016/182065109-4f2cebdb-424c-4aba-8f1b-a2c3d9e08e56.png)
We can see that this model has the lowest balanced accuracy score of all the othe methods at 51%. We can see again, the differences in population sizes between the high risk and low risk populations. This model produced a precision of 1% and a recall of 59% leading to an F1 of 1%. The low risk recall is 43% due to the large number of false positives. 
### SMOTEENN Model
![image](https://user-images.githubusercontent.com/102090016/182065147-e228538d-22ed-4c64-a965-531dce433d71.png)
![image](https://user-images.githubusercontent.com/102090016/182065203-2881c51a-468e-4c28-ac86-7cc11980de8d.png)
![image](https://user-images.githubusercontent.com/102090016/182065259-b2f124cf-9eae-4a87-a08d-db2b4f7b1236.png)
The balanced accuracy score for this model is 63%. This model produced a precision of 1% and a recall of 71% leading to an F1 of 2%. The low risk recall is 54% due to the large number of false positives
### BalancedRandomForestClassifier Model
![image](https://user-images.githubusercontent.com/102090016/182065305-75c6e004-81b5-4abe-812a-a7bb3957e7ca.png)
![image](https://user-images.githubusercontent.com/102090016/182065340-eaed8b93-b98a-498d-9f6f-401a5e27cdde.png)
![image](https://user-images.githubusercontent.com/102090016/182065394-d72eb9c1-fc9c-4cf2-8bf9-14f5437fa0f2.png)
The balanced accuracy score for this model is 79%, leaving it to be the highest accuracy score thus far. The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%. The low risk sensitivity has now increased to 91% with a 100% precision as a result of a low number of false positives.
### Easy EnsembleClassifier Model
![image](https://user-images.githubusercontent.com/102090016/182065486-8faeff9e-2b31-43b9-a8bf-974f6e1b13f3.png)
![image](https://user-images.githubusercontent.com/102090016/182065539-9f70af51-7806-4d83-bb33-60ea638e4114.png)
![image](https://user-images.githubusercontent.com/102090016/182065588-53221e5b-c0cb-4a1f-9318-9bccc864d9d8.png)
This model has the greatest balanced accuracy score of 93%. The high_risk precision is at 7% with a 91% sensitivity which equates to an F1 of 14%. The low_risk sensitivity is now 94% with 100% presicion due to the low number of false positives
## Summary
When looking at the balanced accuracy scores for all of the models we can see that most models fell below the 75% range. The Ensemble methods produced higher scores, specifically the ensemble classifier model. While the model performed greatly in detecing high risk cases with a 93% of detecting a high risk case, the precision was very low at 7%. The low precision means that there are many low risk credit cases that are being falsely detected as high risk. Overall, this method seems to be the strongest option however, the bank may want to seek other methods that allow them to more accurately predit high-risk cases and not let low-risk cases fall through.
