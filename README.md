# Income-Classification

![alt text](https://github.com/LinsiLin/Income-Classification/blob/main/portfolio-3.jpg)

• Table of Contents
• Get the Data
• Data Cleaning
• Exploratory Data Analysis
• Data Preprocessing
• Feature Selection and Clustering
• Classifiers
  • Logistic Regression
  • Decision Tree
  • Random Forests
  • Support Vector Classification
  • K-nearest Neighbors
  • Gaussian Naive Bayes
  • Quadratic Discriminant Analysis
  • AdaBoost
  • Gradient Boosting
  • Multi-layer Perceptron Classifier
  
Imbalanced Dataset
Many learning algorithms were designed assuming well-balanced class distributions, i.e. no significant differences in class prior probabilities. However, this is not always the case in real world data since one class might be represented by a large number of examples, while the others are represented by only a few, and this is the case for this dataset. The target variable "income" has imbalanced distribution with about 25% being '>50K" and 75% being "<=50K".

The solution to the imbalanced data are mainly two types: data level methods and the algorithmic level methods.

Data level methods
Data level methods consist of balancing classes by resampling the original data set, such that under-represented classes are over-sampled, and over-represented classes are under-sampled.

Random over-sampling(non-heuristic method)
It aims to balance class distribution through the random replication of minority class examples. Since it makes exact copies of examples from the minority class, which can increase the likelihood of overfitting.

Oversampling(heuristic method)
There are two approaches supported for generating new data points, Synthetic Minority Over-sampling Technique (SMOTE) and Adaptive Synthetic Sampling (ADASYN). Both techniques use interpolation to generate new datapoints. To be specific, SMOTE is an over-sampling method with synthetic data generation. Its main idea is to form new minority class examples by interpolating between several examples from the minority class that lie together. And ADASYN uses a weighted distribution for different minority class examples according to their level of difficulty in learning, where more synthetic data is generated for minority class examples that are harder to learn compared to those minority examples that are easier to learn.


Random under-sampling(non-heuristic method)
It aims to balance class distribution through the random elimination of majority class examples. But there is critic that under-sampling can eventually discard data potentially important for learning.


Undersampling(heuristic method)
Some heuristic under-sampling methods include NearMiss,Condensed Nearest Neighbor Rule,Tomek links, One-sided selection, Neighborhood Cleaning Rule. I implemented NearMiss, Tomek links and Neighborhood Cleaning Rule in this notebook.
Algorithmic level methods:
Idea: adapting existing algorithms and techniques to the especial characteristics of imbalanced data. These proposals include cost-sensitive learning, one-class classifiers, and ensembles of classifiers, among others.
