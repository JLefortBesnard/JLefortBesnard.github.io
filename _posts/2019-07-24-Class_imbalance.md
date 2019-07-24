---
title: "Stats jam: deal with class imbalance with Python"
author_profile: true
tags: [StatsJam]
---

<p align="justify">
In a dataset including observations belonging to class 0 or class 1, if only 5% of observations belong to class 0, 
then even a naive model that predicts every observation as belonging to class 1 will be 95% accurate. 
Clearly, this is not ideal. Using confusion matrices, precision, recall, F1 scores, and ROC curves is always helpful. In some cases, though,
you actually can deal with this class imbalance.
</p>

There are 4 types of solution:

1. The first and the best way would be to collect more data. 
2. You could change the metrics used to evaluate your model so that the class imbalance is not an issue anymore.
3. You can use a model’s built-in class weight parameters if possible; e.g. randomforest(class_weight="balanced")
4. Finally, if none of the above is feasible, consider downsampling, or upsampling.

<p align="justify">
As a rule of thumb, downsampling is done when the number of observations in the majority class is higher than a third of 
the number of observations in the minority class. However, it is usually considered as better to use upsampling since 
less information is lost.
</p>

We will now see how to downsample and upsample using Python.

## Downsampling the majority class

<p align="justify">
Downsampling means creating a new set of observations from the majority class of size equals to the minority class's size.
Thus, we randomly sample without replacement (we don't want the same observation twice since we have enough observations in 
this class) from the majority class until we reach the size of the minority class.
We first extract the observations' indexes for each different class (here 0 for minority class, 1 for the majority class):
</p>

```
# Indicies of each class' observations
ind_0 = np.where(target == 0)[0]
ind_1 = np.where(target == 1)[0]
```

<p align="justify">
We then get the lenght of each class:
</p>

```
# Number of observations in each class
n_0 = len(ind_0)
n_1 = len(ind_1)
```

<p align="justify">
Finally, we will randomly pick as many observations in the majority class as there are observations in the
minority class:
</p>

```
# For every observation of class 0, randomly sample from majority class without replacement
ind_1_downsampled = np.random.choice(ind_1, size=n_0, replace=False)
```

<p align="justify">
We can now use the indexes that were randomly picked to form the new set of majority class observations and build the 
preprocess dataset with as many observations from the majority class as there are in the minority class.
We join the downsampled set of majority class observations to the set of minority class observations:
</p>

```
# Join together the vectors of target 
np.hstack((target[ind_0], target[ind_1_downsampled]))

# Join together the arrays of features
np.vstack((features[ind_0,:], features[ind_1_downsampled,:]))
```

<p align="justify">
That's it, you can now run your analysis. Don't forget to report this operation in details in the methods section.
</p>

## Upsampling the minority class

<p align="justify">
Downsampling means creating a new set of observations from the minority class of size equals to the majority class's size.
Thus, we randomly sample with replacement from the minority class (we create duplicates on purpose to reach the size of the 
majority class set) until we reach the size of the majority class. So this time, we randomly pick as many observations 
in the minority class as there are observations in the majority class (thus indeed creating duplicates). We keep our example 
thus we have 0 for minority class, 1 for the majority class. Let's downsample:
</p>

```
# For every observation in class 1, randomly sample from class 0 with replacement
ind_0_upsampled = np.random.choice(ind_0, size=n_1, replace=True)
```

<p align="justify">
We can now use the indexes that were randomly picked to form the new set of minority class observations and build the 
preprocess dataset with as many observations from the minority class as there are in the majority class.
We join the upsampled set of minority class observations to the set of majority class observations:
</p>

```
# Join together the vectors of target
np.concatenate((target[ind_0_upsampled], target[ind_1]))

# Join together the arrays of features
np.vstack((features[ind_0_upsampled,:], features[ind_1,:]))
```

<p align="justify">
That's it, you can now run your analysis. Don't forget to report this operation in details in the methods section.
</p>

Source:
Chris Albon (2018). Machine Learning with Python Cookbook. 
