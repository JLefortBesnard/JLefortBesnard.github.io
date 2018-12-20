---
title: "Stats jam: Bayesian hierarchical modelling"
author_profile: true
tags: [StatsJam]
---


At a rule of thumb, if you have less than 100 observations and not a lot of trials, machine learning is not likely to perform well.
If on top, you have a lot of variables (e.g., age, weight, sex, etc...), you are likely to face the multiple comparisons problem if using classical statistics.



The Bayesian hierarchical modeling estimates the parameters of the posterior distribution using the Bayesian method.
"Hierarchical" because information is available on several different levels of observational units 
and we want to separately estimate the posterior distribution of each individual predictor and its group-level effects. 

The Bayesian hierarchical modeling is useful in case of nested data. And we can consider that every dataset is kind of nested. Let's say you have a control group of heatlhy subjects, they could still be divided into subgroups (per gender, age, etc...).
Hierarchical modeling is perfectly adapted to such setting. It fits to dataset with more parameters than observations.
Prof. Gelman suggested to use the Bayesian hierarchical modeling by default.

Nowadays, we have a much richer description of people => more meta-information than before which explains why the Bayesian hierarchical modeling is emerging.
In psychiatry, location is a nested hidden variable rarely exploited. The dataset size is usually quite small and by dividing your sample into subsamples, the risk of
overfitting is increased because of the lack of data. Using a frequentist or a machine learning approach would not deal well with the information lost.
Using the Bayesian hierarchical modeling improves the parameter estimates and reduce the risk of overfitting. It shares the statistical strength by doing partial pooling.


* Great introduction to hierarchical modeling [here](http://mfviz.com/hierarchical-models/)
* More infoon multilevel modeling by Andrew Gelman [here](http://www.stat.columbia.edu/~gelman/research/published/multi2.pdf)
* The Bayesian hierarchical modeling page on [Wikipedia](https://en.wikipedia.org/wiki/Bayesian_hierarchical_modeling) is also great.
