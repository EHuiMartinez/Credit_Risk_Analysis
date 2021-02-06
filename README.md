# Credit_Risk_Analysis

## Overview of the analysis: 
This analysis uses the credit card credit dataset from LendingClub, applied machine learning to predict credit card risk.  In Python, we used scikit-learn and imbalanced-learn libraries to build and evaluate models using resampling algorithms such as Random oversampling, SMOTE, Undersampling and Combination of over and under sampling or SMOTEENN and ensemble models that reduces bias with Balanced Random Forest Classifier and Easy Ensemble Classifier.  Using the results of the algorithms, we can compare which algorithm results in the best performance.

## Results: 
Each of the resampled models produced a balanced accuracy score and a classification report with precision and recall scores of all six machine learning models. Loan status of 'high risk' vs 'low risk' was used from the dataset as target for prediction, the rest of the dataset was used as features.  The dataset was split to train and test data and calculated with balanced accuracy score, confusion matrix and imbalanced classification report with the below results:

### Resampling 

#### Naive Random Oversampling
* Balanced accuracy score: 66%
* Precision scores: high risk= 1%; low risk = 100%; Avg = 99%
* Recall scores: high risk = 68%; low risk = 64%; Avg = 64%
* The accuracy is low at 66%.  Even though the average precision score is high in 99%, it is only effective for low risk predictions (100%), not for high risk (1%). The recall or sensitivity is also low for both high and low risk groups with an average of 64%.

![NaiveRandomOverSampling.png](/Resources/NaiveRandomOverSampling.png)

#### SMOTE Oversampling
* Balanced accuracy score: 65%
* Precision scores: high risk = 1%; low risk = 100%; Avg = 99%
* Recall scores: high risk = 63%; low risk = 67%; Avg = 66%
* The accuracy is low at 65%.  Even though the average precision score is high in 99%, it is only effective for low risk predictions (100%), not for high risk (1%). The recall or sensitivity is also low for both high and low risk groups with an average of 66%.

![SMOTEOverSampling.png](/Resources/SMOTEOverSampling.png)

#### Undersampling
* Balanced accuracy score: 53%
* Precision scores: high risk = 1%; low risk = 100%; Avg = 99%
* Recall scores: high risk = 64%; low risk = 41%; Avg = 42%
* The accuracy is lowest at 53%.  Even though the average precision score is high in 99%, it is only effective for low risk predictions (100%), not for high risk (1%). The recall or sensitivity is also low for both high and low risk groups with the lowest average of 42%.

![UnderSampling.png](/Resources/UnderSampling.png)

#### SMOTEENN - Combination (Over and Under) Sampling
* Balanced accuracy score: 66%
* Precision scores: high risk = 1%; low risk = 100%; Avg = 99%
* Recall scores: high risk = 74%; low risk = 59; Avg = 59%
* The accuracy is low at 66%.  Even though the average precision score is high in 99%, it is only effective for low risk predictions (100%), not for high risk (1%). The recall or sensitivity is also low for both high and low risk groups with an average of 59%.

![ComboOverUnderSampling.png](/Resources/ComboOverUnderSampling.png)

### Ensemble

#### Balanced Random Forest Classifier
* Balanced accuracy score: 79%
* Precision scores: high risk = 3%; low risk = 100%; Avg = 99%
* Recall scores: high risk = 70%; low risk = 87%; Avg = 87%
* Features ranked: The top 10 features that contributes to the predictions vs the bottom features - there are 11 features that have no affect on the predictions.
* The accuracy is high at 79%.  Even though the average precision score is high in 99%, it is only effective for low risk predictions (100%), not for high risk (3%). The recall or sensitivity is high with the high risk group at 70%, the low risk group at 87% and an average of 87%.

![BalancedRandomForestClassifier.png](/Resources/BalancedRandomForestClassifier.png)

*Features ranked - Top & Bottom 10*
![Features_ranked.png](/Resources/Features_ranked.png)

#### Easy Ensemble AdaBoost Classifier
* Balanced accuracy score: 93%
* Precision scores: high risk = 9%; low risk = 100%; Avg = 99%
* Recall scores: high risk = 92%; low risk = 94%; Avg = 94%
* The accuracy is highest at 93%.  Even though the average precision score is high in 99%, it is only effective for low risk predictions (100%), not for high risk (9%). The recall or sensitivity is high with the high risk group at 92%, the low risk group at 94% and an average of 94%.


![EasyEnsembleAdaBoostClassifier](/Resources/EasyEnsembleAdaBoostClassifier.png)


## Summary:

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.##