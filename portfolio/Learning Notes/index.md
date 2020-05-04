---
layout: default
title: Notes
---
This section serves as a placeholder for my notes, so that I can review certain concepts when needed.  				



Key ideas covered: &nbsp;  <a href="L09_regularization__slides 2.pdf" target="_blank">L09_regularization</a> 


[comment]: <Complete Jekyll setup included (layouts, config, [404](/404), [RSS feed](/atom.xml), posts, and [example page](/about))> 

* Common Regularization Techniques, e.g. Early stopping, L<sub>1</sub>/L<sub>2</sub> , and dropout
* Validation set is used for model section, for hyperparameter tuning, tells you info about training 
* High variance, fit data closely so when you switch data, boundary will have high variance than previous line.
* WHy does dropout work well (Slides 35)





Key ideas covered: &nbsp; <a href="L10_norm-and-init__slides.pdf" target="_blank">L10_norm</a> 

* BatchNorm normalizes hidden layer inputs (slides 7)
* BatchNorm has 2 main steps, standardization and learnable scaling
* Backprop for BatchNorm parameters
* BatchNorm provides additional parameters that will help layers to learn a little bit more independently, BatchNorm allows larger learning rates
* BatchNorm becomes more stable with learger minibatch sizes, since s.d. and mean will be too noisy if we use small minibatch size ( each minibatch has their own mean and s.d.)
* We do normalization when feature have different ranges
* Why minibatch sizes as power of 2



---
