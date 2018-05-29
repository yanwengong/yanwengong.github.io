---
layout: post
#标题配置
title:  05_linClassification
#时间配置
date:   2018-05-27 01:08:00 +0800
#大类配置
categories: study_notes
#小类配置
#tag: machine_learning
---

* content
{:toc}


## Linear classification

1. Perceptron classifier: It is a classifier with two features ($$ f = \theta_1X_1 + \theta_2X_2 + \theta_0 $$) plus a threshold function ($$ T(f) $$); the output is a class decision {+1, -1}.   

2. Perceptron is a linear classifier  
  * The parameters $$ \theta $$ are sometimes called weights ("w")  
  * A perceptron first calculates a weighted sum of the input features, then the sum is thresholded by the T(.) function    

3. Class overlap: sometimes classes may not be well-separated and we may not be able to perfectly distinguish between classes. We could try to add more features (features can be quadratic, etc.) or use more complex classifier. Otherwise, may have to accept some errors.  

4. Effect of dimensionality  
  * "good": separation is easier in higher dimensions; increase the number of features, and even a linear classifier will eventually be able to separate all the training examples  
  * "bad": overfitting   

## Learning  

1. Measure the error of a linear classifier  
  * nature measure = "fraction we get wrong": $$ err(\underline{\theta}) = \frac{1}{m}\sum\delta(\hat{y}(i) != y(i)) $$ The problem of this measurement is it is hard to deal with gradient descent since it is not continuous.  

2. Here we introduce a better learning method - perceptron algorithm, which adjusts $$ \theta $$ for each data point j  
  * $$ \hat{y}(j) = T(\underline{\theta} * \underline{x}(j)) $$ : predict output for each data point j  
  * $$ \underline{\theta} = \underline{\theta} + \alpha( y(j) - \hat{y}(j)) \underline{x}(j) $$ : "gradient-like" step  
  * this methods will adjust based on every "wrongly predicted" data and ignore the corrected points; eventually will converge if data are linearly separable   

3. Surrogate loss functions: use a "smooth" function ($$ \sigma $$) and calculate the MSE; $$ J(\underline{\theta}) = \frac{1}{m}\sum( \sigma(f(x^{(j)})) -y^{(j)})^2 $$  
  * if points far from the decision boundary, small error; if nearby the boundary, large error  
<img src="../styles/images/cs273a/surrogate_loss_func.png">
