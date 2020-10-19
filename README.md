# Credit Risk Analysis

## Overview
***Fast Lending***, a peer to peer lending services company wants to use machine learning to predict credit risk. Management believes that this will provide a quicker and more reliable loan experience. It also believes that machine learning will lead to more accurate identification of good candidates for loans which will lead to lower default rates. The company wants me to assist the lead Data Scientist, Jill, in implementing this plan. In my role, I will build and evaluate several machine learning models or algorithms to predict credit risk, I will use techniques such as resampling and boosting to make the most of my models and myr data. Once I've designed and implemented these algorithms, I'll evaluate their performcance and see how well my  models predict data. To accomplish my task, I will dive headlong into machine learning algorithms, statistics, and data processing techniques.

## Purpose of this Analysis
In this analysis, I have to apply machine learning to solve a real-world challenge: credit card risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I’ll need to employ different techniques to train and evaluate models with unbalanced classes.

## Resources
* Software/Tools: Google Colab, Visual Studio Code (v1.49.2), JupyterNotebook
* Language(s): Python
* Data Source(s): https://github.com/Govind-Patwal/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv

## Report on the Credit Risk Analysis


1. Random Oversampler
![RandomOversampler](Resources/1_RandomOversampler.png)

2. SMOTE
![SMOTE](Resources/2_SMOTE.png)
3. Cluster Centroids Resampler
![ClusterCentroids](Resources/3_ClusterCentroids.png)

4. SMOTEENN
![SMOTEENN](Resources/4_SMOTEENN.png)


5. Balanced Random Forest Classifier
![BalancedRandomForestClassifier](Resources/5_BalancedRandomForestClassifier.png)

6. Easy Ensemble Classifier
![EasyEnsembleClassifier](Resources/6_EasyEnsembleClassifier.png)

Deliverable 4: Written Report on the Credit Risk Analysis (30 points)
Deliverable 4 Instructions
For this deliverable, you’ll write a brief summary and analysis of the performance of all the machine learning models used in this Challenge.

The report should contain the following:

Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.


Analysis (24 points)
The written analysis has the following:



There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
