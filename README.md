# Quora-Question-Pair-Similarity

Analysis on various machine learning model to predict whether a pair of questions are duplicates or not.

#nlp #tfidf #machinelearning

Problem statement is taken from Kaggle https://www.kaggle.com/c/quora-question-pairs.
Here various text encoding method is tried and model is finetuned to achiveve best possible accuracy.



## SUMMARY


### Problem Statement

* It is a binary classification problem, for a given pair of questions we need to predict if they are duplicate or not. We are tasked with predicting whether a pair of questions are duplicates or not.

### Use case:

* This could be useful to instantly provide answers to questions that have already been answered. Quora

### Bussiness Impact

* In this way the resource utilization can be optimized. No need to ask for answer again as the Question can be duplicate.


### Data Cleaning

* Univariate analysis is done on each features and ouliers are removed in the dataset.

* Dataset is balanced


### Algorithm Applied


* XGBOOST on set1 with Hyperparameter tuning using Randomsearch

* Logistic Regression (Tfidf_weighted_w2v) (Tf-idf)

* Linear Support Vector Machine (Tfidf_weighted_w2v) (Tf-idf)

* 79% are correctly predicted as Similar Questions which is better all other models

* As we see, both Precision and Recall is good for Similar and Non-similar Questions

* Here 16711 points are correctly predicted as non-duplicate Questions (86%)

* XGboost for set 2 is not tried, since the Dimention of set2 is very high (>20000)


### Feature Engineering

* cwc_min, cwc_max, mean_len, last_word_eq, first_word_eq, csc_min, csc_max, fuzz_ratio, token_sort_ratio
