# GAN-s-for-ART
###### my first project (IEEE mega project)

## What Are GAN's
A **generative adversarial network** *(GAN)* is a class of machine learning systems invented by **Ian Goodfellow** in 2014. Two neural networks contest with each other in a game *(in the sense of game theory, often but not always in the form of a zero-sum game)*. Given a training set, this technique learns to generate new data with the same statistics as the training set. For example, a GAN trained on photographs can generate new photographs that look at least superficially authentic to human observers, having many realistic characteristics. Though originally proposed as a form of generative model for unsupervised learning, GANs have also proven useful for semi-supervised learning, fully supervised learning, and reinforcement learning. 

**Yann LeCun described** GANs as:
> *"the coolest idea in machine learning in the last twenty years"*

## Why is it called as GAN's
### Generative:
It is a generative model, which describes how data is generated in terms of a probabalistic model.
### Adversarial:
The training of the model is done in an adverserial setting, *(i.e. it involves conflit and opposition)*.
### Networks:
We use **DeepLearning(Neural networks)** for building the architecture of the *GAN's* model

## Basic Idea
In *GAN's*, there is a *generator* and a *discriminator*. the generator generates fake images and tries to fool the discriminator. The discriminator on the othe hand tries to distinguish between fake and real samples. Here the generative model cpatures the distribution of data and is traines in cuch a manner that it tries to minimize the probability of the *discriminator* to make a mistake. The *discriminator*, on the other hand is based on a model that estimates the probability that the sample it gets from the training data and the generator is True of  False.
The *GAN's* can be thought as a min-max algorithim, where *discriminator* is trying to maximize its rewards **V(D,G)** and the *generator* is trying to minimize the *discriminators* rewards.
where,
     **P data(x)** = distribution of real data
     **P(z)**      = distribution for *generator*
     **x**         = sample from *P data(x)*
     **z**         = sample from *P(z)*
     **D(x)**      = *discriminator* network
     **G(z)**      = *generator* network

![formula](https://user-images.githubusercontent.com/47821576/63063097-e8f4fa00-bf18-11e9-8fe8-cc4f5a1cfba8.jpg)

### So basically, training the GAN has 2 parts:
#### Part-1:
The *discriminator* is trained while the *generator* is idle. In this phase, the network is only forward propogation and no_backpropagation is done. It is also trained on the fake generated data obtain from the *generator*.
#### Part-2:
The *generator* is trained while the *discriminator* is idle. After the **D(x)** is trained by the generated fake data of **G(z)**, we get its predictions and use the results for training the *generator* and get better results form the previous try and then it again trys to fool the *discriminator* somehow.
