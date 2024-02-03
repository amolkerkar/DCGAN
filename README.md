# Deep Convolutional Generative Adversarial Network (DCGAN) for MNIST
## Overview
This repository contains a PyTorch implementation of a Deep Convolutional Generative Adversarial Network (DCGAN) for learning and generating MNIST digits. DCGAN is a type of Generative Adversarial Network (GAN) architecture designed for image generation tasks. In this project, we use the DCGAN model to learn the distribution of MNIST digits and generate new, realistic-looking digits.

## Dataset
The model is trained on the MNIST dataset, which consists of 28x28 grayscale images of handwritten digits (0-9). The dataset is automatically downloaded by torchvision if it is not available.

## Architecture
### Generator Architecture:
* Input: Random noise vector (nz)
* Output: 28x28 grayscale image
* Transposed convolution layers with batch normalization and ReLU activation functions
* The final layer uses Tanh activation to map the output to the range [-1, 1]
### Discriminator Architecture:
* Input: 28x28 grayscale image
* Output: Probability of input being real or generated
* Convolutional layers with batch normalization and leaky ReLU activation functions
* The final layer uses Sigmoid activation to produce a probability score
