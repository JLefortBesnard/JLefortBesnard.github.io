---
title: "Stats jam: simple things first"
author_profile: true
tags: [StatsJam]
---

<p align="justify">
Professor Robert Tibshirani recently gave a talk about statistical learning. 
He reminded a fundamental formula about trying to extract insights from data: 
"try simple models first and move on to more complex methods, only if necessary".
</p>
<p align="justify">
Going deep directly is barely the best move unless you have a LOT of data. 
If you don’t try simple things first, you will for sure miss important characteristics that could help
to eventually use or design an appropriate model which goes deep. By directly going deep, you are giving up 
with interpretability which is often important in neuroscience though not always needed indeed. 
Most importantly, if you have wide data (number of features bigger than number of observations) 
or if you only have a moderate amount of observations (<500) then a simple LASSO will likely outperform a deep model. 
Deep neural networks (DNNs) usually need large quantity of data to perform well, which is often lacking in neuroimaging. 
In fact, He and colleagues (2018) have shown that DNNs did not outperform Kernel regression using almost 1000 
subjects from the Human Connectome Project for predicting the fluid intelligence using functional 
connectivity (419 x 419 features). In neuroscience, many researchers used a deep neural network (DNN) 
with less than 500 observations, still even more features and claimed a high accuracy. 
A model on such high dimensional data would face the curse of dimensionality (Hastie et al., 2009), 
thus not learn but overfit the observations and fail to generalize. As Bdzdok and Yeo (2017) stated: always keep in mind 
that the huge success of DNNs (in many different application domains) is partly due to colossal sample sizes with 
n > 1,000,000 (LeCun et al., 2015; Jordan et al., 2015). In neuroscience nowadays, the biggest datasets reach about 
1000 participants (Human Connectome Project) to about 10,000 participants (UK Biobank Imaging). Therefore, despite the 
growing literature applying DNNs to neuroscience applications, if you have only a few data at hand, 
and you reach a high accuracy using cross validation, still remind yourself that it might be that you hacked the hell out 
of the hyperparameters and eventually overfitted you sample (including the test set).
</p>

<p align="justify">
[Prof. Tibshirani Talk link](https://www.youtube.com/watch?v=qTYDDhGUK10)
Bzdok, Yeo . Neuroimage, Inference in the age of big data: Future perspectives on neuroscience. 2017
Hastie T, Tibshirani R, Friedman J: The Elements of Statistical Learning: Data Mining, Inference, and Prediction . 2009, Springer, New York City, USA
He, T. et al. (2018) Is deep learning better than kernel regression for functional connectivity prediction of fluid 
intelligence? In 2018 International Workshop on Pattern Recognition in Neuroimaging (PRNI), pp. 1–4, IEEE
M.I. Jordan, T.M. Mitchell. Machine learning: trends, perspectives, and prospects. Science, 349 (2015), pp. 255-260
Y. LeCun, Y. Bengio, G. Hinton. Deep learning. Nature, 521 (2015), pp. 436-444
</p>
