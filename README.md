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
In *GAN's*, there is a *generator* and a *discriminator*. the generator generates fake images and tries to fool the discriminator. The discriminator on the othe hand tries to distinguish between fake and real samples.
