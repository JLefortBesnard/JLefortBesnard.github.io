---
title: "Tips for learning Python and Machine Learning"
author_profile: true
tags: [Learning]
---

# GETTING STARTED WITH PYTHON

## Install the prerequisite (Anaconda package, Atom)
1. Ask the internet "anaconda package download" or directly copy-paste this link: https://www.anaconda.com/download/
3. Select if you're using MAC, Windows or Linux
4. Click on *download Python 3.6* (not 2.7, this version will soon be obsolete)

### What did you just do? 
* **About Python 3**: It's an interpreter (a language). It allows you to "talk" to your machine from the terminal. I suggest you use [ipython3](https://ipython.org/) (included in the Anaconda package). The i stands for "interactive" python. It makes everything more simple. FYI Python was not named after the snake but after the Monty Python :-)
* **About Anaconda**: It is a package including Python 3, ipython and many other useful modules. It also allows to create environments (end of this [video](https://www.youtube.com/watch?v=YJC6ldI3hWk)). In sum, an environment puts everything at the same place in your computer which avoids errors. 
* **About Atom**: Atom is basically a text editor. We use it to write and save scripts, that's it. But atom is quite awesome for several reasons: i) there are several great add ons. For example, one is called flake8 and automatically
corrects your script to make it well written according to the [pep8 standard](https://www.python.org/dev/peps/pep-0008/), ii) it makes the script really easy to read thanks to its color syntax and iii) a lot of short cuts and options make the process of writting scripts easier.

## DIGGING DEEPER

### Free python online classes
* https://external.codecademy.com/learn/python
* http://learnpythonthehardway.org/
* https://github.com/jrjohansson/scientific-python-lectures
* http://programarcadegames.com/
* http://www.pythonchallenge.com/
* https://developers.google.com/edu/python/?hl=de-DE&csw=1
* https://github.com/jrjohansson/scientific-python-lectures
* http://www.grappa.univ-lille3.fr/~coulom/Python/intro.html
* https://wiki.python.org/moin/BeginnersGuide/NonProgrammers
* https://scipy-lectures.org/
* [there](https://github.com/JLefortBesnard/PythonClass), you can find the files I created to give a workshop on Python, it might be useful for complete beginners

As a fun read that explains where Python is situated in the landscape
of programming languages:

* http://developeronline.blogspot.de/2009/04/if-philosophers-were-programmers.html

### Manipulate data with Python with Numpy
* https://www.youtube.com/watch?v=fXhzQRO5YCA
* https://engineering.ucsb.edu/~shell/che210d/numpy.pdf
* https://docs.scipy.org/doc/numpy/reference/

### Manipulate data with Python with Pandas DataFrame
* https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.html
* http://pandas.pydata.org/pandas-docs/stable/10min.html
* https://pandas.pydata.org/pandas-docs/stable/dsintro.html
* https://www.datacamp.com/community/tutorials/pandas-tutorial-dataframe-python

### Working with fMRI/MRI data
* https://nilearn.github.io/auto_examples/index.html


Just go through the examples, you can also copy-paste the scripts into your terminal once you've installed Python and then modify slightly each of them to understand what it does.

### Machine learning with Python
Same here, click on the algorithm you're interested in and read the example script:
* http://scikit-learn.org/stable/index.html

### Plotting
* http://pythonplot.com/#bar-counts
* https://seaborn.pydata.org/
* https://altair-viz.github.io/
* https://matplotlib.org/

### R versus python
* https://blog.dominodatalab.com/video-huge-debate-r-vs-python-data-science/

### Great other links about Python
* Chris Albon [website](https://chrisalbon.com/).
Everything you need to know in Python from preprocessing to deep learning. Scroll down the home page, it's great.
* [realpython](https://realpython.com/) where you can even subscribe to free email series about Python tricks!
* Siraj Raval [Youtube videos](https://www.youtube.com/channel/UCWN3xxRkmTPmbKwht9FuE5A). This guy even made rap songs on machine learning!

**Reminder:** *Programming is a practical skill that is better learned by -doing- rather than -studying-, much like learning foreign languages*

# GETTING STARTED WITH MACHINE LEARNING

## Videos about statistical learning and prerequisite:

* Nando de freitas
[Deep learning](https://www.youtube.com/watch?v=PlhFWT7vAEw) and [Machine learning](https://www.youtube.com/watch?v=4vGiHC35j9s)

* Yoshua Bengio
[Representation learning](https://www.youtube.com/watch?v=O6itYc2nnnM)

* W Gilbert Strang
[Linear algebra](https://www.youtube.com/watch?v=ZK3O402wf1c)

* Andrew NG
[Machine Learning](https://www.coursera.org/learn/machine-learning)

## Great related articles with PDF online:
* "Statistical modeling: The two cultures" [Breiman](https://projecteuclid.org/download/pdf_1/euclid.ss/1009213726)
* "A few useful things to know about machine learning" [Domingos](https://dl.acm.org/citation.cfm?id=2347755)
* "Statistical data analysis in the computer age" [Efron, Tibshirani](http://science.sciencemag.org/content/253/5018/390)
* "Machine learning: Trends, perspectives, and prospects" [Jordan, Mitchell](http://science.sciencemag.org/content/349/6245/255)
* "Classical Statistics and Statistical Learning in Imaging Neuroscience" [Bzdok](https://www.frontiersin.org/articles/10.3389/fnins.2017.00543/full)
* "Element of statistical learning" [Hastie et al](https://web.stanford.edu/~hastie/ElemStatLearn/) 
* "Introduction to statistical learning" [James et al](https://link.springer.com/book/10.1007%2F978-1-4614-7138-7)

## Other interesting links:
* Machine Learning [Flash Cards](https://machinelearningflashcards.com/)
* A bunch of machine learning related [Cheat Sheets](https://www.datasciencecentral.com/page/search?q=cheat+sheets)
* A [list](https://www.bigdatanews.datasciencecentral.com/profiles/blogs/80-best-data-science-books-that-are-worthy-reading) of machine learning books worth reading

# HOW MUCH DO I NEED TO KNOW
It's never easy to start and to understand how far you should go on an online class. Here is a list of the key concepts related to python and machine learning that you should at least have a gross idea if you want to do research in neuroscience. It takes about a year to get a good overview of these stuff.

## Python-related
* Terminology: Python object, Python integer and float, Python list, Python tuple, Python class, Python function, Python dictionary, Python variable, lambda, Numpy array, Numpy nan, Pandas DataFrame, booleans (if, elif, else, etc..), loop (for while), print function, grouping, merging, cleaning datasets, magic command, error, debugging, Pep8, timing code, concatenate, index, feature engineering,  shape, length, UFuncs, method, module, slice, type, data type and structure.
* Libraries or tools name and usage: Pandas, Numpy, Sklearn, Nilearn, matplotlib, seaborn, scipy, torch, tensorflow, iPython, Python function parameter, Jupyter, Atom, Sublime, Git, GitHub, pip, anaconda package.

## Machine Learning-related
* Statistical cultures: Bayesian, machine learning, classical statistics
* Terminology: model, fitting, gradient descent, cost function, overfitting, underfitting, variance, bias, accuracy, cross validation (leave one out, k-fold, nested, etc...), prediction accuracy, prediction, estimation, training-test-validation set, residual sum of squares, inference, model interpretability, coefficients/weights/betas, regularization, shrinkage methods, sparsity, learning, feature selection, feature extraction, input, output, dimension reduction, tuning parameter, high dimensional data, curse of dimensionality, parameter, hyperparameter, smoothing parameter, data type and structure (qualitative, quantitative, scalar, vector, matrix, tensor, etc...), classifier, Kernel, polynomial, constraint, assumption, underlying assumption, ground truth, bagging, boosting, bootstrapping, ensemble learning, joint distribution, computational power, degree of freedom, VC dimension, Gaussian, probability, maximum likelihood estimation, best model, training a model, learning curve, model complexity, algorithms, generalization, Occam's Razor.
* ML model types: tree-based, regression, classification, clustering, dimension reduction, linear/non-linear models, manifold learning, type of learning: supervised/unsupervised/semi-supervised/reinforcement.   
* Most famous models names + how they work and advantages/disadvantages: Kmeans, k-nearest neighbors, linear and logistic regression, Ridge and Lasso, neural network (perceptron, deep neural network: feedforward and recurrent), PCA, ICA, polynomial regression, random forest, SVM.


