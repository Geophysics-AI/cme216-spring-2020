---
layout: page
title: Stanford CME 216 class material
---

These is the web site for CME 216 Machine Learning in Computational Engineering. This material was created by [Eric Darve](https://me.stanford.edu/people/eric-darve), with the [help](https://github.com/EricDarve/cme216-spring-2020/commits/master) of course staff and students.
{% include marginnote.html id='mn-construction' note='The site is **under construction**! If you find errors or feel that some parts need clarification, please let us know, or submit a pull request with your fixes to our [GitHub repository](https://github.com/EricDarve/cme216-spring-2020).'%} The Jekyll theme is inspired by the [CS228 course notes](https://github.com/ermongroup/cs228-notes) site on GitHub.

## Syllabus

[Syllabus](syllabus)

## Reading assignments

Module 1

- [Introduction to ML and SVM](Reading Questions/intro_svm)
- [Soft-margins in SVM](Reading Questions/svm_softmargin)
- [Kernel trick](Reading Questions/kernel_trick)

Module 2

- [Perceptron](Reading Questions/perceptron)
- [MLP](Reading Questions/MLP) (multi-layer perceptron)
- [TensorFlow](Reading Questions/TF)
- [Subclassing](Reading Questions/subclassing)

## Programming Homework

- [Python setup guide](Python Setup Guide)
- [Homework 1](Homework/HW1 Questions) and [starter code](Homework/hw1_starter_code.zip)
- [Homework 2](Homework/HW2 Questions) and [starter code](Homework/hw2_starter_code.zip)

## Lecture slides and code

The videos accompanying these lectures can be found on canvas under ["Course Videos."](https://canvas.stanford.edu/courses/118944/external_tools/3367)

Python tutorial

- [Tutorial code](https://github.com/EricDarve/cme216-spring-2020/tree/master/Code/Python)
- [Python introduction notebook](https://github.com/EricDarve/cme216-spring-2020/blob/master/Code/Python/Python%20basics.ipynb)
- [Numpy notebook](https://github.com/EricDarve/cme216-spring-2020/blob/master/Code/Python/Numpy%20tutorial.ipynb)

Module 1

- [SVM code](https://github.com/EricDarve/cme216-spring-2020/blob/master/Code/svm.ipynb)
- [1.1 Brief introduction to machine learning](Slides/ML_introduction/brief_intro)
- [1.2 A few examples of machine learning](Slides/ML_introduction/examples_ML)
- [1.3 Supervised learning](Slides/ML_introduction/supervised_learning)
- [1.4 Machine learning in engineering](Slides/ML_introduction/ml_in_engineering)
- [1.5 Introduction to SVM](Slides/SVM_introduction/)
- [1.6 Scikit-learn](Slides/scikitlearn/scikit)
- [1.7 Soft-margin](Slides/scikitlearn/softmargin)
- [1.8 Overfitting](Slides/scikitlearn/overfitting)
- [1.9 Training and validation sets](Slides/scikitlearn/training_validation)
- [1.10 Kernel trick](Slides/scikitlearn/kernel_trick)

Module 2

- [2.1 Perceptron](Slides/ANN/perceptron)
- [2.2 Artificial Neural Networks](Slides/ANN/MLP) (multilayer perceptron)
- [2.3 TensorFlow/Keras](Slides/TF_Keras/TF_Pytorch)
- [2.4 Sequential API](Slides/TF_Keras/TF_sequential)
- [2.5 Functional API](Slides/TF_Keras/TF_functional)
- [2.6 Subclassing](Slides/TF_Keras/subclassing)
- [DNN TensorFlow code](https://github.com/EricDarve/cme216-spring-2020/blob/master/Code/DNN_regression.ipynb)
- [Python inheritance example code](https://github.com/EricDarve/cme216-spring-2020/blob/master/Code/Inheritance%20demo.ipynb)

Module 3

- [3.1 Loss function for regression and classification](Slides/Deep_Learning/Loss)
- [3.2 Backpropagation](Slides/Deep_Learning/Backprop)

## Contents of class

Highlight of topics to cover

**Supervised learning and SVM**

Module 1 (week 1 and 2)

- Supervised learning
- SVM; [scikit-learn](https://scikit-learn.org/stable/); kernel trick; radial basis functions
- Overfitting; underfitting; regularization

- Homework 1 due; April 16 (SVM homework)

**Deep learning**

Module 2 (week 3)

- NN and DNN; layers; weights and biases; activation function; loss function
<!-- - Universal approximation theorems; [Montufar et al. (2014)](http://papers.nips.cc/paper/5422-on-the-number-of-linear-regions-of-deep-neural-networks.pdf) -->
- [TensorFlow](https://www.tensorflow.org/learn) and [Keras](https://www.tensorflow.org/guide/keras)

Module 3 (week 4)

- Forward and back-propagation
- Weight initialization
- Regularization; test and validation sets; hyperparameter optimization
- Regularization strategies
<!-- - Batch normalization -->

- Homework 2 due; April 30 (covid-19 modeling)

Module 4 (week 5-6)

- Stochastic gradient methods; SGD, momentum; adaptive algorithms
- Convolution nets; pooling; fully-connected nets
- DNN and convnet architectures

**Physics-informed learning**

Module 5 (week 6-7)

- Physics-based ML; PhysML
- DNN and numerical PDE solvers
- Automatic differentiation; forward and reverse mode AD; chain rule; computational graph
- Examples of numerical PDE solutions with ADCME
- Physics constrained learning

- Homework 3 due on May 14 (week 6; bathymetry)

**Generative deep networks**

Module 6 (week 8-9)

- Autoencoders and variational autoencoders
- GAN to model stochastic variables
- Discriminator network
- WGANs
- PhysGAN

- Homework 4 due on May 28 (week 8; physics informed learning)

**Reinforcement learning**

Module 7 (week 9-10)

- Reinforcement learning; [Sutton and Barto](http://incompleteideas.net/book/the-book.html); [Mnih 2013](https://arxiv.org/abs/1312.5602)
- Temporal difference learning; deep Q-learning networks
- Policy gradients and actor-critic algorithms

- Short homework 5 on RL (June 11)

## Reading material

###  Books

- [Deep learning](http://www.deeplearningbook.org/) by Ian Goodfellow and Yoshua Bengio and Aaron Courville
- [Deep learning: an introduction for applied mathematicians](https://epubs.siam.org/doi/pdf/10.1137/18M1165748) by Catherine Higham and Desmond Higham
- [Machine learning: a probabilistic perspective]() by Kevin Murphy
- [Deep learning with Python](https://searchworks.stanford.edu/view/13216992) by Fran&#231;ois Cholet
- [Deep learning illustrated: a visual, interactive guide to artificial intelligence](https://searchworks.stanford.edu/view/13463749) by Jon Krohn
- [Neural networks and deep learning](http://neuralnetworksanddeeplearning.com/) by Michael Nielsen
- [Foundations of machine learning](https://cs.nyu.edu/~mohri/mlbook/) by Mehryar Mohri, Afshin Rostamizadeh, and Ameet Talwalkar
- [Elements of statistical learning](https://searchworks.stanford.edu/view/12458005) by Trevor Hastie, Robert Tibshirani, and Jerome Friedman
- [Neural networks and learning machines](https://searchworks.stanford.edu/view/8631715) by Simon Haykin
- [The matrix cookbook](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf) by Kaare Petersen and Michael Pedersen

### Video tutorials

- [Introduction to deep learning: concepts and fundamentals](https://searchworks.stanford.edu/view/13216564) by Laura Graesser
- [Introduction to deep learning models with TensorFlow: learn how to work with TensorFlow to create and run a TensorFlow graph, and build a deep learning model](https://searchworks.stanford.edu/view/13214579) by Lucas Adams
- [Deep learning with TensorFlow: applications of deep neural networks to machine learning tasks](https://searchworks.stanford.edu/view/13215423) by Jon Krohn

### Review papers

- LeCun, Bengio and Hinton, Deep learning, _Nature,_ 521:436-444, 2015
- Schmidhuber, Deep learning in neural networks: an overview, _Neural Networks,_ 61:85-117, 2015
- [Automatic differentiation in machine learning: a survey](https://arxiv.org/pdf/1502.05767.pdf) by At&#305;l&#305;m G&uuml;nes Baydin, Barak Pearlmutter, Alexey Andreyevich Radul, and Jeffrey Mark Siskind
- [A review of the adjoint-state method for computing the gradient of a functional with geophysical applications](https://academic.oup.com/gji/article/167/2/495/559970) by R.-E. Plessix

### Online classes and tutorials

- [Introduction to Deep Learning](http://introtodeeplearning.com/), MIT
- [fast.ai](https://course.fast.ai/)
- [Machine Learning 2014-2015](https://www.cs.ox.ac.uk/people/nando.defreitas/machinelearning/), Oxford, by Nando de Freitas

### Links

- [List of books and tutorials on ML](https://github.com/josephmisiti/awesome-machine-learning/blob/master/books.md)
- [Online courses](https://github.com/josephmisiti/awesome-machine-learning/blob/master/courses.md)
- [TensorFlow notebooks](https://github.com/the-deep-learners/TensorFlow-LiveLessons) by Jon Krohn
- [TF2 notebooks](https://github.com/jonkrohn/tf2) by Jon Krohn
- [Deep learning illustrated notebooks](https://github.com/the-deep-learners/deep-learning-illustrated) by Jon Krohn
- [TensorFlow playground](http://playground.tensorflow.org/)
- [MNIST visualization](https://www.cs.ryerson.ca/~aharley/vis/conv/) by Adam Harley
- [Distill](https://distill.pub/), a journal for machine learning visualizations