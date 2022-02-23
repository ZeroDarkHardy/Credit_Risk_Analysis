# Credit_Risk_Analysis

## Overview of Project

Given a dataset of consumer credit profiles, this project aims to build and test several different types of machine learning models to analyze and predict credit risk.  Six different models/sampling methods were employed, and then compared based on balanced accuracy score, precision score, and recall score.

### Index

- Results:
    - [Naive Random Oversampling](#naive-random-oversampling-model)
    - [SMOTE Oversampling](#smote-oversampling-model)
    - [Cluster Centroids Undersampling](#cluster-centroids-undersampling-model)
    - [SMOTEENN Combination Sampling](#smoteenn-combination-over-and-undersampling-model)
    - [Balanced Random Forest Classifier](#balanced-random-forest-classifier-model)
    - [Easy Ensemble Adaboost Classifier](#easy-ensemble-adaboost-classifier-model)
- [Summary](#summary)

## Resources

Source Data: [LoanStats_2019Q1.csv](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/resources/LoanStats_2019Q1.csv)<br/>
Software: Visual Studio Code v1.64.2, Jupyter Notebook 6.4.6, Python 3.7.11, Conda 4.11.0

---

## Results

### Naive Random oversampling model

![naive_random_oversampling.png](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/images/naive_random_oversampling.png)<br/>
- Balanced Accuracy Score: 64.8%<br/>
- Precision Score(high risk / low risk): 1% / 100%<br/>
- Recall Score(high risk / low risk): 63% / 66%<br/>

### SMOTE oversampling model

![smote_oversampling.png](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/images/smote_oversampling.png)<br/>
- Balanced Accuracy Score: 62.4%<br/>
- Precision Score(high risk / low risk): 1% / 100%<br/>
- Recall Score(high risk / low risk): 62% / 63%<br/>

### Cluster Centroids undersampling model

![cluster_centroids_undersampling.png](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/images/cluster_centroids_undersampling.png)<br/>
- Balanced Accuracy Score: 51.3%<br/>
- Precision Score(high risk / low risk): 1% / 100%<br/>
- Recall Score(high risk / low risk): 59% / 44%<br/>

### SMOTEENN (combination over and undersampling model)

![smoteenn.png](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/images/smoteenn.png)<br/>
- Balanced Accuracy Score: 62.2%<br/>
- Precision Score(high risk / low risk): 1% / 100%<br/>
- Recall Score(high risk / low risk): 70% / 54%<br/>

### Balanced Random Forest Classifier model

![balanced_random_forest_classifier.png](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/images/balanced_random_forest_classifier.png)<br/>

### List of features, in descending order:
![feature_importances.png](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/images/feature_importances.png)<br/>
- Balanced Accuracy Score: 78.8%<br/>
- Precision Score(high risk / low risk): 4% / 100%<br/>
- Recall Score(high risk / low risk): 67% / 91%<br/>

### Easy Ensemble Adaboost Classifier model

![easy_ensemble_adaboost.png](https://github.com/ZeroDarkHardy/Credit_Risk_Analysis/blob/main/images/easy_ensemble_adaboost.png)<br/>
- Balanced Accuracy Score: 92.5%<br/>
- Precision Score(high risk / low risk): 7% / 100%<br/>
- Recall Score(high risk / low risk): 91% / 94%<br/>

---

## Summary

All six models show fairly weak precision in detecting high risk credit, though the Ensemble classifiers showed much higher sensitivity in that category. With such weak precision (between 1-7%, respectively), our client is to have far more false negatives than false positives.  While that means that the bank is very unlikely to end up financing an account that they shouldn't have, the number of business opportunities that they miss out on is far greater.  Overall, the strongest model seems to be the EasyEnsemble Adaboost classifier, which had slightly higher precision than the rest (7% for high_risk) and much higher sensitivity than most (91% for high_risk).<br/>

On the whole, I wouldn't recommend our client utilize any of these models until they can be better trained, and I believe that effort should be focused on the EasyEnsemble Adaboost Classifier, since it has produced the most promising results thusfar.