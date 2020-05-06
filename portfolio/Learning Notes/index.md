---
layout: post
title: Notes
---
This section serves as a placeholder for my notes, so that I can review certain concepts when needed.  				



Key ideas covered: &nbsp;  <a href="L09_regularization__slides 2.pdf" target="_blank">L09_regularization</a> 


[comment]: <Complete Jekyll setup included (layouts, config, [404](/404), [RSS feed](/atom.xml), posts, and [example page](/about))> 

* Common Regularization Techniques, e.g. Early stopping, L<sub>1</sub>/L<sub>2</sub> , and dropout
* Validation set is used for model section, for hyperparameter tuning, tells you info about training 
* High variance, fit data closely so when you switch data, boundary will have high variance than previous line.
* WHy does dropout work well (Slides 35)



Tricks for training NN more efficiently

Key ideas covered: &nbsp; <a href="L10.pdf" target="_blank">L10_norm</a> 

* BatchNorm normalizes hidden layer inputs, so that it not only affects the first hidden layer but also the layers afterward (slides 7)
* BatchNorm has 2 main steps, standardization and learnable scaling
* Backprop for BatchNorm parameters
* BatchNorm provides additional parameters that will help layers to learn a little bit more independently, BatchNorm allows larger learning rates
* BatchNorm becomes more stable with learger minibatch sizes, since s.d. and mean will be too noisy if we use small minibatch size ( each minibatch has their own mean and s.d.)
* We do normalization when feature have different ranges
* Why minibatch sizes as power of 2

Part 2: Weight initialization

* Symmetry create problem because backpropogation would update each unit the same weight
* We want our weight account for the number of incoming unit
* TanH is the rescaled version of sigmoid, but it has a steeper gradient and center at zero, wider output range
* Xavier Initialization is develped under TanH
* Method for Xavier Initialization (2 steps)
* To prevent the gradients of the network’s activations from vanishing or exploding, The variance of the activations should stay the same across every layer, but variance depends on the number of input, make sure the activation function are not saturated, and that we have a gradient.





---
