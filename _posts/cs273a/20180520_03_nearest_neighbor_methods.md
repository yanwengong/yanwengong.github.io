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
* Equation to calculate the Euclidean distance: $$ d(x, x`) = \sqrt{\sum_{i}(x_{i}-x`_{i})^2} $$
