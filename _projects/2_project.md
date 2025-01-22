---
layout: page
title: ML Olympiad - Autism Prediction Challenge
description: A Two-Level Stacking Ensemble Classifier for Autism Prediction
img: assets/img/projects/autism_prediction.png
importance: 2
category: personal
related_publications: false
---

### Overview

This project presents an advanced machine learning solution developed for the ML Olympiad's Autism Prediction Challenge. The system implements a sophisticated two-level stacking ensemble classifier that combines multiple powerful algorithms to achieve high-accuracy autism prediction. By addressing the inherent challenges of unbalanced medical data and employing robust validation techniques, the system achieved remarkable performance with an AUC-ROC score of 0.943 on the test set.

### Architecture

The system's architecture is built around a two-level stacking ensemble that strategically combines multiple base estimators with a meta-learner. The first level consists of four powerful base classifiers: XGBoost, LightGBM, CatBoost, and Random Forest. These diverse algorithms each bring their unique strengths to the ensemble, capturing different aspects of the underlying patterns in the data. The second level employs a Logistic Regression model as the meta-learner, which learns to optimally combine the predictions from the base estimators.

### Data Processing and Balance

A critical challenge in medical diagnosis problems is dealing with unbalanced datasets, where one class (typically the negative class) significantly outnumbers the other. To address this, the system implements the SMOTE (Synthetic Minority Over-sampling Technique) algorithm. SMOTE creates synthetic examples of the minority class by interpolating between existing instances, helping to balance the dataset without simple replication of existing samples. This approach ensures that the model learns equally well from both positive and negative cases.

### Model Training and Validation

The training process employs stratified k-fold cross-validation to ensure robust performance evaluation across all data segments. This technique maintains the same proportion of samples for each class in all folds, which is particularly important given the unbalanced nature of the dataset. The validation strategy provides reliable performance estimates and helps prevent overfitting.

### Hyperparameter Optimization

To maximize model performance, the system utilizes a Bayesian tuning framework for hyperparameter optimization. This approach efficiently explores the hyperparameter space for each base estimator and the meta-learner, making intelligent decisions about which combinations to try based on previous results.

### Technical Implementation

The implementation leverages several key machine learning libraries and techniques:

- Scikit-learn for the base Random Forest classifier and meta-learner
- XGBoost, LightGBM, and CatBoost for gradient boosting implementations
- Imbalanced-learn library for SMOTE implementation
- Optuna for Bayesian hyperparameter optimization
- Scikit-learn's StratifiedKFold for cross-validation
