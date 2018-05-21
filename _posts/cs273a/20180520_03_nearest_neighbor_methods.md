---
layout: post
#标题配置
title:  03_knn
#时间配置
date:   2018-05-20 01:08:00 +0800
#大类配置
categories: study_notes
#小类配置
#tag: machine_learning
---

* content
{:toc}


## Nearest neighbor methods
* One method to make prediction is through regression model, which is suggesting a
relationship between x and y, then estimate y(new) given new observed x(new).
Another way is through nearest neighbor regression - find training datum x(i) closet
to x(new) then use y(i) as the prediction of y(new).
* Equation to calculate the Euclidean distance:
$$ d(x, x^{\prime}) = \sqrt{\sum_{i}(x_{i}-^{\prime}_{i})^2} $$  
* Imaging the area of features composed as countless points, by calculating the
distance from the known points to the countless points, we can assign each known point
a region which has the same y value, where all points in the region are closer to this point than others. Decision boundary is the edge between regions. In general, nearest-neighbor classifier produces piecewise linear decision boundary.   

## Nearest neighbor methods: K-Nearest Neighbors (kNN)  
* How to make classification by kNN: 1. find the k-nearest neighbors to x in the data; calculate Euclidean distance and select k vector with the smallest distance; 2. make prediction based on regression: average the y-values of the k closest training examples and use the result as predicted value OR make classification: rank the y value of the k feature vectors and pick the class which is most common in the set.   
* kNN decision boundary: increasing k "simplifies" decision boundary   
* error rates and k: if k = 1, zero error for training data, but the predictive error will be high which is overfitting; should use validation data to estimate test error rate and select k
