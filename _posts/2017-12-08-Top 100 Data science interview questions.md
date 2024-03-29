---
layout: post
title: Top 100 Data science interview questions
published: true
---
Data science, also known as data-driven decision, is an interdisciplinery field about scientific methods, process and systems to extract knowledge from data in various forms, and take descision based on this knowledge. A data scientist should not only be evaluated only on his/her knowledge on mahine learning, but he/she should also have good expertise on statistics. 
I will try to start from very basics of data science and then slowly move to expert level. So let's get started.

### 1.  What is the difference between supervised and unsupervised machine learning?
#### Supervised Machine learning:
Supervised machine learning requires training labeled data. 
#### Unsupervised Machine learning: 
Unsupervised machine learning doesn't required labeled data. 

### 2. What is bias, variance trade off ?
#### Bias:  
"Bias is error introduced in your model due to over simplification of machine learning algorithm." 
It can lead to underfitting. When you train your model at that time model makes simplified assumptions to make the target function easier to understand.
##### Low bias machine learning algorithms - Decision Trees, k-NN and SVM 
##### Hight bias machine learning algorithms - Liear Regression, Logistic Regression

#### Variance: 
"Variance is error introduced in your model due to complex machine learning algorithm, your model learns noise also from the training dataset and performs bad on test dataset."
It can lead high sensitivity and overfitting.

Normally, as you increase the complexity of your model, you will see a reduction in error due to lower bias in the model. However, this only happens till a particular point. As you continue to make your model more complex, you end up over-fitting your model and hence your model will start suffering from high variance.

![Bias variance trade off](https://i.imgur.com/a7UKJO8.png)

#### Bias, Variance trade off: 
The goal of any supervised machine learning algorithm is to have low bias and low variance to achive good prediction performance.
1. The k-nearest neighbors algorithm has low bias and high variance, but the trade-off can be changed by increasing the value of k which increases the number of neighbors that contribute to the prediction and in turn increases the bias of the model.

2. The support vector machine algorithm has low bias and high variance, but the trade-off can be changed by increasing the C parameter that influences the number of violations of the margin allowed in the training data which increases the bias but decreases the variance.

There is no escaping the relationship between bias and variance in machine learning.

Increasing the bias will decrease the variance.
Increasing the variance will decrease the bias.


### 3. What is exploding gradients ?
"Exploding gradients are a problem where __large error gradients__ accumulate and result in very large updates to neural network model weights during training."
At an extreme, the values of weights can become so large as to overflow and result in NaN values.

This has the effect of your model being unstable and unable to learn from your training data. 
Now let's understand what is the gradient.
#### Gradient: 
Gradient is the __direction and magnitude__ calculated during training of a neural network that is used to update the network weights in the right direction and by the right amount. 

### 4. What is a confusion matrix ?
The confusion matrix is a 2X2 table that contains 4 outputs provided by the __binary classifier__.  Various measures, such as error-rate, accuracy, specificity, sensitivity, precision and recall are derived from it.
_Confusion Matrix_

![](https://i.imgur.com/NYozwa5.png)

A dataset used for performance evaluation is called test dataset. It should contain the correct labels and predicted labels.

![observed-labels.png](https://i.imgur.com/64mZwRG.png)

The predicted labels will exactly the same if the performance of a binary classfier is perfect.

![perfect-classifier.png](https://i.imgur.com/HeVTzab.png)

The predicted labels usually match with part of the observed labels in real world scenarios. 

![regular-classifier.png](https://i.imgur.com/hqNvN2N.png)
 
 A binary classifier predicts all data instances of a test dataset as either positive or negative. This produces four outcomes-
 1. True positive(TP) - Correct positive prediction
 2. False positive(FP) - Incorrect positive prediction
 3. True negative(TN) - Correct negative prediction
 4. False negative(FN)  - Incorrect negative prediction 
 
 ![perfect-classifier.png](https://i.imgur.com/WxQLV83.png)
 
 __Basic measures derived from the confusion matrix__
 1. Error Rate = (FP+FN)/(P+N)
 2. Accuracy = (TP+TN)/(P+N)
 3. Sensitivity(Recall or True positive rate) = TP/P
 4. Specificity(True negative rate) = TN/N
 5. Precision(Positive predicted value) = TP/(TP+FP)
 6. F-Score(Harmonic mean of precision and recall) = (1+b)(PREC.REC)/(b^2PREC+REC) where b is commonly 0.5, 1, 2.
 
 
### 6. Explain how a ROC curve works ?
The __ROC__ curve is a graphical representation of the contrast between true positive rates and false positive rates at various thresholds. It is often used as a proxy for the trade-off between the sensitivity(true positive rate) and false positive rate.

![Imgur](https://i.imgur.com/HjGC4Zb.png)
 
### 7. What is selection Bias ?
Selection bias occurs when sample obtained is not represantative of the population intended to be analyzed.
 
### 8. Explain SVM machine learning algorithm in detail.
SVM stands for support vector machine, it is a supervised machine learning algorithm which can be used for both __Regression and Classification__. If you have n features in your training dataset, SVM tries to plot it in n-dimentional space with the value of each feature being the value of a particular coordinate. SVM uses hyper planes to seperate out different classes based on the provided kernel function. 

![regular-classifier.png](https://i.imgur.com/dU1GDSe.png)

### 9. What are support vectors in SVM. 

![SVM](https://i.imgur.com/DmBOr8Y.jpg)

In the above diagram we see that the thinner lines mark the distance from the classifier to the closest data points called the support vectors (darkened data points). The distance between the two thin lines is called the margin.

### 10. What are the different kernels functions in SVM ? 
There are four types of kernels in SVM.
 1. Linear Kernel
 2. Polynomial kernel
 3. Radial basis kernel
 4. Sigmoid kernel
 
### 11. Explain Decision Tree algorithm in detail.
Decision tree is a supervised machine learning algorithm mainly used for the __Regression and Classification__.It breaks down a dataset into smaller and smaller subsets while at the same time an associated decision tree is incrementally developed. The final result is a tree with decision nodes and leaf nodes. Decision tree can handle both categorical and numerical data. 
 
![Imgur](https://i.imgur.com/Y4jdwtw.png)

### 12. What is Entropy and Information gain in Decision tree algorithm ?
The core algorithm for building decision tree is called __ID3__. __ID3__ uses __Enteropy__ and __Information Gain__ to construct a decision tree. 

__Entropy__

A decision tree is built top-down from a root node and involve partitioning of data into homogenious subsets. __ID3__ uses enteropy to check the homogeneity of a sample. If the sample is completely homogenious then entropy is zero and if the sample is an equally divided it has entropy of one. 

![Imgur](https://i.imgur.com/XFE0f6V.png)


__Information Gain__ 

The __Information Gain__ is based on the decrease in entropy after a dataset is split on an attribute. Constructing a decision tree is all about finding attributes that returns the highest information gain.

![Imgur](https://i.imgur.com/KI934dk.png)

![Imgur](https://i.imgur.com/rZcG68J.png)


### 13. What is pruning in Decision Tree ?
When we remove sub-nodes of a decision node, this procsss is called pruning or opposite process of splitting. 


### 14. What is Ensemble Learning ?
Ensemble is the art of combining diverse set of learners(Individual models) togather to improvise on the stability and predictive power of the model. Ensemble learning has many types but two more popular ensemble learning techniques are mentioned below.

__Bagging__

Bagging tries to implement similar learners on small sample populations and then takes a mean of all the predictions. In generalized bagging, you can use different learners on different population. As you expect this helps us to reduce the variance error.

![Imgur](https://i.imgur.com/1pE4VTo.png)

__Boosting__

Boosting is an iterative technique which adjust the weight of an observation based on the last classification. If an observation was classfied incorrectly, it tries to increase the weight of this observation and vice versa. Boosting in general decreases the bias error and builds strong predictive models. However, they may overfit on the training data. 

![Imgur](https://i.imgur.com/mH85e7T.png)

### 15. What is Random Forest? How does it work ?
Random forest is a versatile machine learning method capable of performing both regression and classification tasks. It is also used for dimentionality reduction, treats missing values, outlier values. It is a type of ensemble learning method, where a group of weak models combine to form a powerful model. 

In Random Forest, we grow multiple trees as opposed to a single tree. To classify a new object based on attributes, each tree gives a classification. The forest chooses the classification having the __most votes__(Over all the trees in the forest) and in case of regression, it takes the __average__ of outputs by different trees. 

### 16. What cross-validation technique would you use on a time series dataset. 
Instead of using k-fold cross-validation, you should be aware to the fact that a time series is not randomly distributed data - It is inherently ordered by chronological order. 

In case of time series data, you should use techniques like forward chaining -- Where you will be model on past data then look at forward-facing data. 

fold 1: training[1], test[2]

fold 1: training[1 2], test[3]

fold 1: training[1 2 3], test[4]

fold 1: training[1 2 3 4], test[5]

### 17. What is logistic regression? Or State an example when you have used logistic regression recently.
Logistic Regression often referred as logit model is a technique to predict the binary outcome from a linear combination of predictor variables. For example, if you want to predict whether a particular political leader will win the election or not. In this case, the outcome of prediction is binary i.e. 0 or 1 (Win/Lose). The predictor variables here would be the amount of money spent for election campaigning of a particular candidate, the amount of time spent in campaigning, etc.

### 18. What do you understand by the term Normal Distribution?

![Imgur](https://i.imgur.com/fvYTdej.jpg)

Data is usually distributed in different ways with a bias to the left or to the right or it can all be jumbled up. However, there are chances that data is distributed around a central value without any bias to the left or right and reaches normal distribution in the form of a bell shaped curve. The random variables are distributed in the form of an symmetrical bell shaped curve.

### 19. What is a Box Cox Transformation?

Dependent variable for a regression analysis might not satisfy one or more assumptions of an ordinary least squares regression. The residuals could either curve as the prediction increases or  follow skewed distribution. In such scenarios, it is necessary to transform the response variable so that the data  meets the required assumptions. A Box cox transformation is a statistical technique to transform non-normal dependent variables into a normal shape. If the given data is not normal then most of the statistical techniques assume normality. Applying a box cox transformation means that you can run a broader number of tests.

![Imgur](https://i.imgur.com/v8j0w3X.jpg)

A Box Cox transformation is a way to transform non-normal dependent variables into a normal shape. Normality is an important assumption for many statistical techniques, if your data isn’t normal, applying a Box-Cox means that you are able to run a broader number of tests.
The Box Cox transformation is named after statisticians ___George Box___ and ___Sir David Roxbee Cox___ who collaborated on a 1964 paper and developed the technique.

### 20. How will you define the number of clusters in a clustering algorithm?

Though the Clustering Algorithm is not specified, this question will mostly be asked in reference to K-Means clustering where “K” defines the number of clusters. For example, the following image shows three different groups.
![Imgur](https://i.imgur.com/qgRH8Rm.jpg)

Within Sum of squares is generally used to explain the homogeneity within a cluster. If you plot WSS for a range of number of clusters, you will get the plot shown below. The Graph is generally known as Elbow Curve.

![Imgur](https://i.imgur.com/iMqv2OG.png)
Red circled point in above graph i.e. Number of Cluster =6 is the point after which you don’t see any decrement in WSS. This point is known as bending point and taken as K in K – Means.This is the widely used approach but few data scientists also use Hierarchical clustering first to create dendograms and identify the distinct groups from there.

### 21. What is deep learning?

Deep learning is subfield of machine learning inspired by structure and function of brain called artificial neural network. We have a lot numbers of algorithms under machine learning like Linear regression, SVM, Neural network etc and deep learning is just an extention of Neural networks. In neural nets we consider small number of hidden layers but when it comes to deep learning algorithms we consider a huge number of hidden latyers to better understand the input output relationship. 

![Imgur](https://i.imgur.com/tMkdwUj.png)

### 22. What are Recurrent Neural Networks(RNNs) ?

Recurrent nets are type of artifical neural networks designed to recognize pattern from the sequence of data such as Time series, stock market and goverment agencis etc. To understand recurrent nets, first you have to understand the basics of feedforward nets. Both these networks RNN and feedforward named after the way they channel information throgh a series of mathematical oprations performed at the nodes of the network. One feeds information throgh straight(never touching same node twice), while the other cycles it throgh loop, and the latter are called recurrent.

![Imgur](https://i.imgur.com/nO6gRVw.png)

Recurrent networks on the other hand, take as their input not just  the current input example they see, but also the what they have percieved previously in time. The BTSXPE at the bottom of the drawing represents the input example in the current moment, and CONTEXT UNIT represents the output of the previous moment. The decision a recurrent neural network reached at time t-1 affects the decision that it will reach one moment later at time t. So recurrent networks have two sources of input, the present and the recent past, which combine to determine how they respond to new data, much as we do in life.

The error they generate will return via backpropagation and be used to adjust their weights until error can’t go any lower. Remember, the purpose of recurrent nets is to accurately classify sequential input. We rely on the backpropagation of error and gradient descent to do so.

Backpropagation in feedforward networks moves backward from the final error through the outputs, weights and inputs of each hidden layer, assigning those weights responsibility for a portion of the error by calculating their partial derivatives – ∂E/∂w, or the relationship between their rates of change. Those derivatives are then used by our learning rule, gradient descent, to adjust the weights up or down, whichever direction decreases error.

Recurrent networks rely on an extension of backpropagation called backpropagation through time, or BPTT. Time, in this case, is simply expressed by a well-defined, ordered series of calculations linking one time step to the next, which is all backpropagation needs to work.

![Imgur](https://i.imgur.com/0esriHM.png)
























 
 # To Be Continued... 
 
 
 
 
 

 




  

