---
title: "Stats jam: variance-covariance"
author_profile: true
tags: [StatsJam]
---

<p align="justify">
In our lab, we have a 30 minutes meeting each week about a specific topic of machine learning or statistics in general. 
Today was about getting a better grasp of variance and covariance.
</p>
### Variance
<p align="justify">
It is the expectation of the squared deviation of a random variable from its mean. How far a set of random numbers are 
spread out from their average value. It gives a measure of how much values of a function of a random variable x vary 
as we sample different values of x from its probability distribution. If the variance is low, then all values of f(X) cluster near their expected value.
The variance is invariant with respect to change in a location parameter (variance is unchanged when adding a constant to all values in a dataset).
The sample variance is a consistent estimator, meaning that it converges to correct values as the number of sample increases.
Usually divided by N-1 to eliminate bias. The sample variance is sensitive to oultiers.
* Var(X) = E[(X-µ)] with E = expected value = the long-run average value of repetitions of the experiment it represents. In other words, the underlying "true" value of a parameter.
* Units of measurement: square of the units of the variable itself (unlike absolute expected deviation which doesn't have units)
</p>
### Covariance
<p align="justify">
It is the measure of how two random variables will change together. It defines the joint variability of two random variables. 
If the greater values of one variable mainly correspond to the greater values of the other variable, and the same holds for the lesser values, 
the covariance is then positive (negative if the opposite pattern is found). The sign of the covariance shows the tendency in the linear relationship
between the two variables. It measures the linear dependence between 2 variables. It's the linear gauge of dependence. The magnitude is difficult to interpret if not normalized. 
The normalized version of the covariance is simply the Pearson correlation coefficient. It gives the goodness of the fit for the best possible linear function describing the relation between 2 variables.
A high absolute covariance means that values change very much and are both far from their respective means at the same time.
</p>
* Cov(X, Y) = E[(X- E[X])(Y- E[Y])] = E[X, Y] - E[X]E[Y] 
Covariance of 2 random variables = population parameter (joint probability distribution)

Sample covariance = estimated value of the population parameter

Special case of covariance when 2 variables are identical: Cov(X, X) = Var(X)

For 2 variables to be independent: 
* Cov(X, Y) = 0 

However, it is not enough because we are omitting the potential non-linear relationship.
Two correlated variables are not independent but two uncorrelated variables do not ensure independence.
One should avoid to talk about correlation but should say linear dependency instead.
