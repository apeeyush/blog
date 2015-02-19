---
layout: post
title:  "Kaggle Contests"
date:   2015-01-22 11:00:00
comments: true
---

I started participating in kaggle contests in December 2014. This post contains my notes for things I have learnt so far. It is still a work in progress.

# Important things for performing well in competitions:

1. Setup env for rapid iteration and experimentation. Use tools like git, sklearn, ggplot2
2. Feature extraction
3. Feature engineering
4. Prevent overfitting
5. Have patience

# General flow:
Extract and select features -> Train models -> Evaluate and visualize results -> Identify and handle data oddities -> Data Preprocessing -> ..REPEAT..

If dataset it too large, consider splitting it.

# Text Learning

Some of the important feature engineering techniques are

- toLowerCase
- spell corrector
- porting
- unigrams-trigrams

The porter stemming algorithm is a efficient preprocessing step on many english language tasks. Eg. connects -> connect; connecting -> connect etc.

# Most useful algorithms

Random Forests, Support Vector Machine, Gradient Boosting Machines -> Blending

SVM, RF, NN, GBM and Multiple Linear Regression
Hierarchical ensemble to combine models

RF and GBM perform very well for common classification and regression tasks

Model ensembling usually results in marginal but significant performance gains (Regularisation + diff models provide different way of looking.. 1%-5%)

# Feature selection

The boruta feature selection algorithm is robust and reliable

- Wrapper method around random forest and it's calculated variable importance
- Iteratively train RFs and runs statistical tests to identify features as important or not important
- Widely used in competition winning models to select a small subset of features for use in training more complex models

# Deep Learning in computer vision competitions

Useful libraries:

- caffe
- Theano
- Torch7

Downsampling dataset


# PCA
Mean normalisation and feature scaling before applying PCA.

Compression: Choose k by % of variance retained (~99%)

Visualization: for k = 2 or 3

**Misuse of PCA**:

- To prevent overfitting - Might work OK but isn't a good way to address overfitting.. Use regularization instead - PCA does not use labels (y) .. so reduces info.. PCA more likely to throw away useful information
- Only if using original features won't work, consider using PCA (Eg. large data - slow/disk space)

[Machine learning best practices by Chief Scientist at Kaggle]: https://www.youtube.com/watch?v=9Zag7uhjdYo
