# Credit Risk Analysis

## Overview
***Fast Lending***, a peer to peer lending services company wants to use machine learning to predict credit risk. Management believes that this will provide a quicker and more reliable loan experience. It also believes that machine learning will lead to more accurate identification of good candidates for loans which will lead to lower default rates. The company wants me to assist the lead Data Scientist, **Jill**, in implementing this plan. In my role, I will build and evaluate several machine learning models or algorithms to predict credit risk, I will use techniques such as resampling and boosting to make the most of my models and my data. Once I've designed and implemented these algorithms, I'll evaluate their performance and see how well my models predict data. To accomplish my task, I will dive headlong into machine learning algorithms, statistics, and data processing techniques.

## Purpose of this Analysis
In this analysis, I have to apply machine learning to solve a real-world challenge: credit card risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I’ll need to employ different techniques to train and evaluate models with unbalanced classes. As a part of this analysis, I have to do the following:
* Oversample the data using the `RandomOverSampler` and `SMOTE` algorithms
* Undersample the data using the `ClusterCentroids` algorithm. 
* Use a combinatorial approach of over- and undersampling using the `SMOTEENN `algorithm. 
* Compare two new machine learning models that reduce bias, `BalancedRandomForestClassifier` and `EasyEnsembleClassifier`, to predict credit risk. 
* Evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Resources
* Software/Tools: Google Colab, Visual Studio Code (v1.49.2), Jupyter Notebook
* Language(s): Python
* Libraries: Pandas, Numpy, scikit-learn, imbalanced-learn
* Data Source(s): https://github.com/Govind-Patwal/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv

## Results

1. **Naive Random Oversampling** (Image below)
    * Precision: High Risk = 0.01; Low Risk = 1.00 
    * Recall: High Risk = 0.74; Low Risk = 0.58
    * Balanced Accuracy Score = 0.66
    * Accuracy score is very less

    ![RandomOversampler](Resources/1_RandomOversampler.png)

2. **SMOTE Oversampling** (Image below)
    * Precision: High Risk = 0.01; Low Risk = 1.00
    * Recall: High Risk = 0.62; Low Risk = 0.68
    * Balanced Accuracy Score = 0.65
    * Accuracy score is again very less

    ![SMOTE](Resources/2_SMOTE.png)

3. **Cluster Centroids Undersampling** (Image below)
    * Precision: High Risk = 0.01; Low Risk = 1.00
    * Recall: High Risk = 0.66; Low Risk = 0.43
    * Balanced Accuracy Score = 0.54
    * Accuracy score went down as compared to the last algorithm

    ![ClusterCentroids](Resources/3_ClusterCentroids.png)

4. **SMOTEENN (Combination of Over and Undersampling)** (Image below)
    * Precision: High Risk = 0.01; Low Risk = 1.00
    * Recall: High Risk = 0.77; Low Risk = 0.54
    * Balanced Accuracy Score = 0.66
    * Accuracy score has imporved over last algorithm but still low

    ![SMOTEENN](Resources/4_SMOTEENN.png)


5. **Balanced Random Forest Classifier** (Image below)
    * Precision: High Risk = 0.03; Low Risk = 1.00
    * Recall: High Risk = 0.70; Low Risk = 0.87
    * Balanced Accuracy Score = 0.79
    * Accuracy Score is reasonaly good, much better than the 4 algorithms above

    ![BalancedRandomForestClassifier](Resources/5_BalancedRandomForestClassifier.png)

6. **Easy Ensemble AdaBoost Classifier**
    * Precision: High Risk = 0.09; Low Risk = 1.00
    * Recall: High Risk = 0.92; Low Risk = 0.94
    * Balanced Accuracy Score = 0.93
    * Accuracy score is very good - the best amongst all 6 algorithms

    ![EasyEnsembleClassifier](Resources/6_EasyEnsembleClassifier.png)

## Summary
* Overall the 2 Ensemble performed way better than the Oversampling/Undersampling/Combination algorithms. 
* The worst algorithm in terms of accuracy is `Cluster Centroids Undersampling` with a score of 0.54, while the best is `Easy Ensemble AdaBoost Classifier` with a score of 0.93
* The low-risk precision score is the same across the board - 1.00
* The high-risk precesion score is the best in the case of `Easy Ensemble AdaBoost Classifier` at 0.09 and combined lowest in all Oversampling/Undersampling/Combination algorithms at 0.01.
* The Oversampling/Undersampling/Combination algorithms also fare poorely than the Ensemble algorithms in terms of recall scores for both high-risk and low-risk loans.

### Recommendation
**AdaBoost**: It clearly stood out with 93% Accuracy score. It also has the highest high-risk and low-risk recall scores. Finally, another very important place where it does much better as compared to others is the high-risk precision score - in this score it is 3x that of the algorithm with the second highest precision score, and 9x that of the majority of the algorithms - this means it is 3-9 times more likely to spot high-risk loans, which if unspotted can have serious consequences for any lender. 