This repository contains a classifier model trained with Car Evaluation Dataset(Source:[Kaggle](https://www.kaggle.com/datasets/elikplim/car-evaluation-data-set)).
The main challenge with the dataset is that most the features are categorical and we can't give these categorical features directly to a machine learning model.
We need to convert these categorical features into real values to train a machine learning model.


In this repo I used ordinal encoder to convert these categorical features into numerical values with proper mapping from category level to numerical value and trained a SVC(Support Vector Classifier).
Though the dataset is having class imbalance with 1434 data points for one class and 120 data points for other class,achived 93% test accuracy.


To tackle the problem of class imbalance I used SMOT(synthetic minority oversampling technique).\n
1.SMOT is a synthetic minority oversampling technique.\n
2.A problem with imbalanced classification is that there are too few examples of the minority class for a model to effectively learn the decision boundary.\n
3.One way to solve this problem is to oversample the examples in the minority class. This can be achieved by simply duplicating examples from the minority class in the training dataset prior to fitting a model. This can balance the class distribution but does not provide any additional information to the model.\n
4.SMOTE first selects a minority class instance a at random and finds its k nearest minority class neighbors. The synthetic instance is then created by choosing one of the k nearest neighbors b of a point a, at random and connecting a and b to form a line segment in the feature space. The synthetic instances are generated as a convex combination of the two chosen instances a and b.


   

