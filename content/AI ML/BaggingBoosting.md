---
title: "Bagging & Boosting in Machine Learning World"
date: "2020-07-04T10:52:27-04:00"
draft: false
---
In my last tech blog, I discussed on Decision trees and Random Forrest. So I thought of articulating on Gradient Boosting model and XgBoost. But before these algorithms , its important to understand 2 basic concepts :
* Bagging  (Bootstrap Aggregation)       
* Boosting

### Bagging (Bootstrap Aggregation)
Bootstrapping is a process of creating random samples with replacement for estimating sample statistics. With replacement means , the sample might have duplicated values from the original set.

For example:
```
Sample S = {10,23,12,11,34,11,1,4,2,14}

Bootstrap sample 1:               {10, 23, 11, 4, 2, 14, 11}

Bootstrap sample 2                {23, 10, 12, 11, 14, 2, 14} – 14 is duplicate (which means with replacement in bootstrap sample set)

Bootstrap sample n :   {10, 1, 2, 2, 14, 1, 23}
```

### Reason to create BootStrap samples

Once bootstrap samples are created, model classifier is used for training or building a model and then selecting model based on popularity votes.

In case of a classification model, a label with maximum votes will assigned to the observations.

In case of a regression model - average value is used.

Bagging is an ensembling process – where a model is trained on each of the bootstrap samples and the final model is an aggregated models of the all sample models.
Refer to below diagram to understand the Bagging process

{{< figure src="/images/baggingboost.jpg" >}}

For [confidence interval](http://hosted.jalt.org/test/PDF/Brown35.pdf)

### Sample Code in Python for Bagging
[Databricks link for Bagging](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/2718522690254083/197903457957926/4283590658906401/latest.html)

### Boosting
In layman’s term , it is a process to convert the weak learners to strong learners

Consider our life where we develop life skills by learning from our mistakes, we can train our model to learn from the errors predicted and improvise the model’s prediction .
Source

* Step 1:  The base learner takes all the distributions and assign equal weight or attention to each observation.
* Step 2: If there is any prediction error caused by first base learning algorithm, then we pay higher attention to observations having prediction error. Then, we apply the next base learning algorithm.
* Step 3: Iterate Step 2 till the limit of base learning algorithm is reached or higher accuracy is achieved.

Finally, it combines the outputs from weak learner and creates a strong learner which eventually improves the prediction power of the model. .

### Types of Boosting algorithms

* Ada-Boost
* Gradient Boosting algorithm
* XgBoost (Oe of the popular ones in Kaggle J )

### Source

* https://web.stanford.edu/class/stats202/content/lec20.pdf     
* https://www.analyticsvidhya.com/blog/2015/11/quick-introduction-boosting-algorithms-machine-learning/     
* https://medium.com/analytics-vidhya/boosting-bagging-and-stacking-a-comparative-analysis-e6b213d416b9
* https://towardsdatascience.com/ensemble-methods-bagging-boosting-and-stacking-c9214a10a205
* https://cse.iitk.ac.in/users/piyush/courses/ml_autumn16/771A_lec21_slides.pdf
* https://medium.com/greyatom/a-quick-guide-to-boosting-in-ml-acf7c1585cb5
* https://machinelearningmastery.com/implement-bagging-scratch-python/       
* https://machinelearningmastery.com/ensemble-machine-learning-algorithms-python-scikit-learn/
