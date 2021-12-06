# Credit_Risk_Analysis

## Overview
Our goal for this project was to build out an algorithm to determine the risk level of loans from a list of loans. We used things like credit limits, loan amounts, bankruptcy and settlement history, etc. to determine the outcome, high-risk or low-risk. We have brought in and trained 6 different machine learning algorithms to see if we could figure out WHICH method would provide the most helpful outcome. We needed to try several methods becuase there was a severe imbalance in the data set we used to train and test our algorithm. With 347/68817 (.5%) loans being considered high risk, 

## Results
The algorithms and thier classifiers are as follows:
- **Naive Random Oversampling** - duplicating occurance of high-risk loan data points for machine training purposes
- ![alt text](https://github.com/Jlew112/Credit_Risk_Analysis/blob/main/Challenge/NaiveRandomOversamplingClassificationReport.PNG?raw=true)
- **SMOTE Oversampling** - creating new high-risk data points based on existing known high-risk data points
- ![alt text](https://github.com/Jlew112/Credit_Risk_Analysis/blob/main/Challenge/SMOTEOversamplingClassificationReport.PNG?raw=true)
- **Undersampling** - decreasing the number of low-risk loan data points to match the number of high-risk points
- ![alt text](https://github.com/Jlew112/Credit_Risk_Analysis/blob/main/Challenge/UnderSamplingClassificationReport.PNG?raw=true)
- **SMOTEENN** - combining over AND under sampling where there is significant data loss to attempt to improve accuracy metrics
- ![alt text](https://github.com/Jlew112/Credit_Risk_Analysis/blob/main/Challenge/SMOTEENNClassificationReport.PNG?raw=true)
- **Random Forest Classifier** - a series of yes/no decision trees meant to test the importance of each variable in relation to the high/low risk outcome
- ![alt text](https://github.com/Jlew112/Credit_Risk_Analysis/blob/main/Challenge/RandomForestClassificationReport.PNG?raw=true)
- **Easy Ensemble AdaBoost Classifier** - a combination of many different smaller algorithms
- ![alt text](https://github.com/Jlew112/Credit_Risk_Analysis/blob/main/EasyEnsembleClassiciationReport.PNG?raw=true)

Each algorithm has its strengths and weaknesses, but we needed to make sure we used the one that would work best for OUR needs. 

## Summary
The Random Forest Classifier, as shown above, had the best F1 score, whcih shows the best combination of Precision and Sensitivity. Since our Precision was VERY close or equal on all of our algorithms, the sensitivity shows the variance between them. The Random Forest Classifier gave us the highest sensitivity, and the fewest missed high-risk loans. This algorithm was able to better predict the high-risk loans, so this is the one I recommend moving forward.
