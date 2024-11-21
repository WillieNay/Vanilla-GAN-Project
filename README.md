# Generative Adversarial Network (GAN) for MNIST Dataset

This project implements a Generative Adversarial Network (GAN) using PyTorch to generate handwritten digits resembling the MNIST dataset.

## Overview

A GAN consists of two neural networks, a Generator and a Discriminator, which are trained together in an adversarial setting:
- **Generator (G)**: Creates fake images from random noise.
- **Discriminator (D)**: Distinguishes between real and fake images.

The goal is to train the generator to produce realistic images that can fool the discriminator.

---

## Features

- Implementation of GAN with PyTorch
- Generates realistic 28x28 handwritten digits
- Saves generated images and model checkpoints
- Adversarial training for iterative improvement

---
Models
Generator (G):

Takes a random noise vector (latent vector) as input.
Generates an image of size 28x28 pixels resembling handwritten digits.
Discriminator (D):

Takes an image as input.
Outputs a probability indicating whether the image is real or fake.
Training Process
Adversarial Training:

The generator tries to produce realistic images to fool the discriminator.
The discriminator tries to correctly classify real and fake images.
Both models improve iteratively, leading to better fake images over time.
Loss Functions:

Binary Cross-Entropy Loss (BCE Loss) is used for both generator and discriminator training.
Optimization:

Both models are optimized using Adam Optimizer.
Dataset
MNIST:
A dataset of handwritten digits (0-9) with 60,000 training images.
The images are normalized to have a mean of 0.5 and a standard deviation of 0.5.

---

Parameters
latent_size: Size of the random noise vector used as input to the generator (default: 64).
hidden_size: Number of hidden units in the generator and discriminator (default: 256).
image_size: Flattened size of the 28x28 image (default: 784).
num_epochs: Number of training epochs (default: 200).
batch_size: Number of samples per batch (default: 100).
Output
The script saves:

Real Images: Samples from the MNIST dataset.
Generated Images: Fake images created by the generator.
Training Progress: Printed to the console, showing discriminator loss (d_loss), generator loss (g_loss), and performance metrics D(x) (real images) and D(G(z)) (fake images).
