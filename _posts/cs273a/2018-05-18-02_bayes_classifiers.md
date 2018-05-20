---
layout: post
#标题配置
title:  02_bayes_classifiers
#时间配置
date:   2018-05-18 01:08:00 +0800
#大类配置
categories: study_notes
#小类配置
#tag: machine_learning
---

* content
{:toc}


## Bayes Classifiers
* The most basic classifier: for each value of features, calculate the most likely
output
* Bayes rule: Covariates are independent given "cause"  
$$ P(y|x) = \frac{P(x|y) * P(y)}{P(x)} $$;
* Naive Bayes Gaussian models: for each features, the probability is Gaussian distribution  
$$ p(x_{1}) = \frac{1}{Z_{1}}exp{-\frac{1}{2\theta_{1}^2}(x_{1}-u_{1})^2} $$  
$$ p(x_{2}) = \frac{1}{Z_{2}}exp{-\frac{1}{2\theta_{2}^2}(x_{2}-u_{2})^2} $$  
$$ p(x_{1})p(x_{2}) = {-\frac_{1}{2}(x-u)^T\sum_^{-1}(x-u)} $$


## Bayes Classifiers: Measuring Error
* Bayes Error Rate: make optimal decision at any particular x;
$$ ErrorRate = [1-maxc p(y=c|x)] $$

## Likelihood Ratio Tests
* Likelihood ratio: relative support for observation x under "alternative hypothesis" y=1,
compared to "null hypothesis" y = 0.
* Log likelihood ratio:
$$ \log[p(x|y=1) / p(x|y=0)] $$

## Roc curves
* true positive rate (sensitivity) vs false positive rate (1 - specificity)
* AUC (area under the roc curve) can be used to measure the performance

## Gaussian Bayes Classifiers  
* TO BE CONTINUED...
