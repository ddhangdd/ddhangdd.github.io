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


* BatchNorm normalizes hidden layer *inputs*, so that it not only affects the first hidden layer but also the layers afterward (slides 7)
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

Key ideas covered: &nbsp; <a href="L10.pdf" target="_blank">L11_norm</a>


Learning rate decay, goal is to coverge minibatch oscillation
If we decrease the learning rate too early, the network doesn't learn anymore and the performance will be worse

1) Exponential Decay
2) Halving
3) Inverse 

Momentum Learning:
Momentum move in the averaged direction of the last few updates. It helps avoid getting stuck on flat surfaces and local minimum in general (slides 31)


Adaptive Learning:
Adaptive Learning Rate
- decrease learning if the gradient changes its direction
- increase learning if the gradient stays consistent

2 steps (slides 41)


>The key advantage of using minibatch as opposed to the full dataset goes back to the fundamental idea of stochastic gradient descent1.
>
>In batch gradient descent, you compute the gradient over the entire dataset, averaging over potentially a vast amount of information. It takes lots of memory to do that. But the real handicap is the batch gradient trajectory land you in a bad spot (saddle point).
>
>In pure SGD, on the other hand, you update your parameters by adding (minus sign) the gradient computed on a single instance of the dataset. Since it's based on one random data point, it's very noisy and may go off in a direction far from the batch gradient. However, the noisiness is exactly what you want in non-convex optimization, because it helps you escape from saddle points or local minima(Theorem 6 in [2]).  The disadvantage is it's terribly inefficient and you need to loop over the entire dataset many times to find a good solution.
>
>The minibatch methodology is a compromise that injects enough noise to each gradient update, while achieving a relative speedy convergence.


Key ideas covered: &nbsp; <a href="L10.pdf" target="_blank">L12_norm</a>

CNN

CNN extract features from the images

CNN basics: Slide 13
Sparse-connectivity 
Parameter sharing
Many layer

* 
the information on the borders of images are not preserved as well as the information in the middle.
To overcome these problems, we use padding.

---
