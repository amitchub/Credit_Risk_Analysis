# Credit_Risk_Analysis
## Overview of the analysis: 
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the data was oversampled using the RandomOverSampler and SMOTE algorithms.  Next, the data was undersampled using the ClusterCentroids algorithm.  After that, a combinatorial approach of over- and undersampling using the SMOTEENN algorithm was used.   Next, two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, were compared to predict credit risk. Finally, an evaluation of the performance of these models is presented, as well as a recommendation on whether they should be used to predict credit risk.

## Results: 
- Oversampling using Naive Random Oversampling
* Accuracy Score: 64.64%
* Precision
  * High Risk: 0.01
  * Low Risk: 1.00
* Recall
  * High Risk: 0.71
  * Low Risk: 0.58

- Oversampling using SMOTE Oversampling
* Accuracy Score: 65.86%
* Precision
  * High Risk: 0.01
  * Low Risk: 1.00
* Recall
  * High Risk: 0.63
  * Low Risk: 0.68


- Undersampling using Cluster Centroids
* Accuracy Score: 65.86%
* Precision
  * High Risk: 0.01
  * Low Risk: 1.00
* Recall
  * High Risk: 0.69
  * Low Risk: 0.40


- Using Combination of Over and Under Sampling
* Accuracy Score: 54.42%
* Precision
  * High Risk: 0.01
  * Low Risk: 1.00
* Recall
  * High Risk: 0.72
  * Low Risk: 0.57


- Using Balanced Random Forest Classifier
* Accuracy Score: 78.85%
* Precision
  * High Risk: 0.03
  * Low Risk: 1.00
* Recall
  * High Risk: 0.70
  * Low Risk: 0.87


- Easy Ensemble Classifier
* Accuracy Score: 93.16%
* Precision
  * High Risk: 0.09
  * Low Risk: 1.00
* Recall
  * High Risk: 0.92
  * Low Risk: 0.94

## Summary: 
The first 4 methods exhibited accuracy from 55%-65%.  All high-risk precision scores for this cohort are 0.01, which implies larger amounts of false positives.  Taken another way, too many low-risk loans would be marked as high-risk to use this moving forward.  All low-risk precision score for this cohort are 1.0, which is a good score.  The lower recall scores are somewhat troubling, and imply that the model is not adequately predicting loan classifications.

The last two methods exhibited much higher accuracy scores.  Precision and recall are also higher, which imply that the models are better at predicting the correct classification.

### Recommendation
The Easy Ensemble Classifier would be the model to use going forward, as it presents the best precision, accuracy, and recall scores.
