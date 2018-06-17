---
layout: post
#标题配置
title:  1_DS_prep_stats_probability
#时间配置
date:   2018-06-12 01:08:00 +0800
#大类配置
categories: study_notes
#小类配置
tag: bittiger
---

* content
{:toc}


## Stats & Probability

1. stats: based on observation (sample), predict the fact (population)
2. probability: based on the population, calculate the probability of the samples

## Sampling

There are several different methods of sampling.
1. random
2. stratified: Town A has 1 million factory workers, Town B has 2 million office workers and Town C has 3 million retirees.  We choose to take a random sample of 10, 20 and 30 from Town A, B and C respectively then we can produce a smaller error in estimation for the same total size of sample.
3. proportion: Town A has 1 million factory workers, Town B has 2 million office workers and Town C has 3 million retirees. We take 1/200 from 1 million in A; 1/200 from 2 million in B and 1/200 from 3 million in C.   

## Probability  

1.
$$ P(A\cupB) = P(A) + P(B) - P(AB) $$  
$$ P(A\cupB\cupC) = P(A) + P(B) + P(C) - P(AB) - P(BC) - P(AC) + P(ABC) $$   

2. Conditional probability:
P(B|A) = P(A and B) / P(A)    
Consider Bayes $$ P(B|A) = \frac{P(A|B)P(B)}{P(A)} $$    

3. Total probability:

$$ P(A) = P(A\capB) + P(A\cap\bar{B}) = P(A|B)P(B) + P(A|\bar{B})P(B)    
P(A\capB) = P(A|B)P(B) $$    

4. Bayes  

$$ P(A|B) = \frac{P(B|A)P(A)}{P(B)} $$         

5. Normal distribution (Gaussian distribution)   
<img src="{{'/styles/images/bittiger_DS/normal_dist_equation.png'}}" width="100%" />      
<img src="{{'/styles/images/bittiger_DS/normal_dist_plot.png'}}" width="100%" />     

Standard normal distribution: u = 0 and deviation = 1.      

6. Binomial distribution (there is only two results)     
$$ P(x = k) = C_{n}^{k} P^{k} (1-P)^{n-k} = \frac_{n!} $$    

7. Poisson distribution   
The Poison distribution is popular for modelling the number of times an event occurs in an interval of time or space.   
<img src="{{'/styles/images/bittiger_DS/poisson_dist_equation.png'}}" width="100%" />      
<img src="{{'/styles/images/bittiger_DS/poisson_dist_plot.png'}}" width="100%" />     
Please note, the event should be independent in Poisson distribution.   

8. Exponential distribution (also known as negative exponential distribution)   
It's about the probability of the gap between the event happening. It's memoryless.
Events are independent.   
<img src="{{'/styles/images/bittiger_DS/exponential_dist_equation.png'}}" width="100%" />      
<img src="{{'/styles/images/bittiger_DS/exponential_dist_plot.png'}}" width="100%" />     

9. Chi-squared test   
Used to test whether there is a significant difference between expected frequencies and the observed frequencies.    
