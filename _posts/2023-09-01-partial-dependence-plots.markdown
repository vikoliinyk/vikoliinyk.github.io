---
title: "Partial Dependence Plots"
layout: post
date: 2023-09-01 17:10
tag: 
- PDP
- ICE
- explainability
headerImage: true
projects: true
hidden: true 
description: "PDPs are awesome and here is why"
category: project
author: viktoriiaoliinyk
externalLink: false
---

### Motivation
Although we have feature importances from the non-linear ML models, they show only a relative change in the target with respect to change in a particular feature, so we can not directly interpret them as for how much change in the target is caused due to a unit change in a particular feature, keeping all other features constant.

Moreover, feature importances don’t show in which direction the feature is influencing the target/
The idea is to isolate the changes made in predictions to solely come from a specific feature. 

It is different than scatter plot of `X` vs. `Y` as scatter plot does not isolate the direct relationship of `X` vs. `Y` and can be affected by indirect relationships with other variables on which both `X` and `Y` depend.

Individual Conditional Expectation (ICE) curves and classical Partial Dependence Plots (PDPs) show an isolated effect of the chosen feature F on the target variable

### ICE curves
For every sample in the original dataset, we fix the values of all the features except the chosen feature `X`.

We change the values of the chosen feature `X`, and predict the target variable. Hence, for every sample and possible values of `X` within its range (on the grid), we have a predicted target. 
Every sample thus corresponds to a single curve on the ICE curves plot, and shows how the changes in the `X` influence the target when other features fixed.

### Classical Partial Dependence Plots
Essentially, classical PDPs are averages of the ICE curves with standard deviation ranges.
For every possible value of `X` within its range (on the grid), we predict the target for all the samples in the dataset and take the mean. 
We also plot the standard deviation around the means.

### Algorithm
1. Train a random forest model (assume `X1, ..., X4` are your features and `Y` is the target variable. Suppose `X1` is the most important feature). 

We are interested to explore the direct relationship of `Y` and `X1`
3. replace column `X1` with `X1(grid_0)` and find new predictions for all observations. take mean of predictions. (call it <i>base value</i>)
4. Repeat step 3 for `X1(grid_1) ... X1(grid_k)`, i.e. for all distinct values of feature `X1`. 
5. PDP’s `X`-axis has distinct values of `X1` and `Y`-axis is change in mean prediction for that `X1` value from base value.