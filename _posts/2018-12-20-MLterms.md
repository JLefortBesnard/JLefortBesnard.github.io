---
title: "Machine learning common terms"
author_profile: true
tags: [StatsJam]
---

### Prediction vs inference
The main goal in statistical learning is to estimate f. Depending on your goal, there could be two reasons to estimate f, you might want to predict or to infer. Prediction means that we want to approximate f as well as possible. Inference means that we want to understand the relationship between X and Y (f is not the main focus). If your goal is to predict, then you will try to find a model g close to f that gives a good approximation of Y. If your goal is to infer, then you will try to make g as readable as possible which will allow you to interpret the model. 

### Parametric vs non-parametric 
Depending on your priors on the problem you want to solve, you might use a parametric or a non-parametric method. The first one involves 1) making an assumption about the shape of f (ex: linear) and 2) fit or train the model (e.g., optimisation using gradient descent). The non-parametric method however, doesn't make any explicit assumption about the shape of f, it fits several possible shapes for f. The main problem of the parametric approach is that the true f might be completely different from our assumption (ex: we try to fit a linear regression whereas f is highly non-linear). For the non-parametric, we don't have this problem since no assumption is made but it needs a very large number of data points.

### Supervised vs unsupervised learning
There are three principal types of learning:
Supervised, reinforcement and unsupervised learning. In the supervised learning, we got a dataset with inputs and outputs (x1 -> y1, x2 -> y2, ..., xm -> ym). In the reinforcement learning, we don't get explicitly the correct outputs. In the unsupervised learning, we don't have any output.

### Regression vs classification 
Depending on the nature of the outcomes, there could be two kinds of problem: Regression and classification. In regression, Y is composed of continuous values. In classification, Y is composed of class label (for example 0 and 1). In regression, we usually aim to estimate or predict a response. In classification, we aim to identify group membership.
 
### Interpretability vs prediction accuracy
A model could be more or less restrictive, leading to more or less flexibility. A very restrictive model is relatively inflexible, it can produce only a small range of shapes to estimate f. A flexible model will allow a broader range of shapes to estimate f. Choosing which one is more adapted depends on your problem: If you are interested in making prediction, you will care more about prediction accuracy than model complexity (meaning you want a good approximate of f which will give you a prediction y' close to y), if you want to infer, then you want a simple model, highly interpretable (g(X) = 3X + 2 is more interpretable than g(X) = 2X³ + 3X²). However in some cases, complexity is not synonymous of high prediction accuracy and can lead to overfitting.
 
### No free-lunch theorem + model assessment
The no free-lunch theorem states that no one method is better than the others over all data sets. Meaning that there is a need to assess the model accuracy. In order to evaluate your model on a given dataset, the most commonly-used measure in the regression settings is the mean squared error (MSE). It is the total difference between the real Y (from f) and the predicted Y' (from g). The bigger the MSE, the bigger the bias (g moves away from f). A model with a low MSE might be considered as having a high prediction accuracy because the predicted Y' are really close to the true Y. Be careful though, it can lead to overfitting. In the classification setting, the metric used to assess how well a model works is usually the percentage of good classifications.

### The bias-variance trade off
As seen before, the bias is the error introduced by trying to approximate f. The higher the bias, the more different g is from f. The variance on the other hand, is the amount by which g would change if using a different dataset. In general, more flexible models got higher variance and less bias. Rigid models are usually biased but bring low variance. 

### Training and test set
We often only have a limited dataset to determinate g. If we use the whole dataset to fit our model g, we won't be able to assess its prediction accuracy on new data (new data means that the algorithm didn't learn using them). One strategy to remedy this problem is the validation set approach. It involves to randomly split the dataset into a training and a validation set (test set). We use the training set to fit the model, and the validation set to assess its accuracy. There are different methods to get a training and a test set. The most common are the k-fold cross-validation and the leave-one-out cross-validation. The first one divides the data set into k fold and each will play the role of training and test set. In the second approach, each data point will play the role of test set. 

### Overfitting and underfitting
After fitting our model using the training set, we will assess it using the test set. A very high training set accuracy does not guarantee a good generalization. If our model fits our training set very well (very low MSE), but the test accuracy is very bad, then the model overfitted the data meaning that it also fitted the noise present in our training set. A low accuracy on the test set might also reflect underfitting which means that the model was not flexible enough to learn relevant patterns in the data.
 
### classical statistics vs Statistical learning notation and goals
 <img src="{{ site.url }}{{ site.baseurl }}/images/MLterms.png" alt="ML terms">
