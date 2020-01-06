# Genetic Algorithms
The goal of this folder is to present different genetic algorithms that I develloped in order to tackle optimization problems in my different jobs. It includes the evolutionnary algorithms that I created but also the different visualizations that I coded/adapted in order to give some insight on how the algorithms operates.
Of course the visualization don't work for all the algorithms (that can operate on continuous or discrete spaces) and I will try to explain which one are the best fitted for each case.
This is more an experimental folder where I suggest an approach and would like to exchange about the relevance of some of my technical choices, I am open to suggestions :) .

## Introduction
These tools were implemented in order to have a more efficient way to solve black-box optimization problems. What I call a black-box is process that can be fed with a given set of inputs and that produces one or multiple outputs. The user doesn't have access to the inner workings of the black box only the output. Therefore a black-box optimization problem is a problem of finding the set of inputs that gives the global minima (or maxima) of the output without knowing how the information (ie the inputs) is processed by the black-box. This can be difficult because the black-box can have multiple local minimas, can be highly non-convex and can have zones of the input space that generate errors.

This is problematic because usually in optimization problems we can access to gradients that allow a faster (and more stable as well) convergence. However here we don't have access to them. A lot of industrial problems have to be formulated as black-box problems, some old codes that don't return their gradients, brute force searches, features selection or even hyper-optimization of statistical models can all be formulated as black box problems. I offer here a way to solve them which is not optimal but surely offers (provided the algorithms are correctly tuned) a better way than a brute force approach (I believe).

## A bit of context
The approaches for tackling black-box problem are numerous and genetic algorithm is a small part of them, [scikit learn](https://scikit-optimize.github.io/) provides a lot of optimizers already (with some of the most recent approaches) but I offer here (I hope) an easier introduction and interpretability of the inner workings of the optimization process
