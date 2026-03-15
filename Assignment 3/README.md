# IE 7615 – Assignment 3

## Overview

This assignment focuses on generative representation learning using **Autoencoders and Variational Autoencoders (VAE)**.

The goal is to analyze how different neural architectures affect **image reconstruction quality and latent space representation**. Experiments are conducted on the MNIST handwritten digit dataset.

The assignment explores:
- Standard Convolutional Autoencoders
- Variational Autoencoders (VAE)
- Effect of different convolution filter sizes
- Latent space interpolation for image morphing

The experiments also investigate how **model capacity influences reconstruction loss and latent space smoothness**. 

---

## Dataset

Dataset used for the experiments:

* Dataset: **MNIST Handwritten Digit Dataset**
* Source: `keras.datasets.mnist`
* Images: 28 × 28 grayscale digits
* Total classes: 10 digits (0–9)

The dataset is widely used for evaluating generative models and representation learning.

---

## Preprocessing

Before training the models, the dataset was prepared using the following steps:

* Images normalized to the range **[0,1]**
* Reshaped to include **channel dimension**
* Split into **training and testing sets**
* Data formatted to support **convolutional neural networks**

Normalization ensures stable training and faster convergence.

---

## Models Implemented

### 1️⃣ Convolutional Autoencoder

Architecture

Encoder
- Conv Layer 1
- Conv Layer 2
- Conv Layer 3
- Latent representation

Decoder
- Transposed Conv Layer 1
- Transposed Conv Layer 2
- Transposed Conv Layer 3
- Reconstructed image output

Experiments were performed with three different filter configurations:

| Configuration | Conv Layers (Encoder) |
| ------------- | --------------------- |
| Config 1      | 128, 64, 32           |
| Config 2      | 256, 128, 64          |
| Config 3      | 512, 256, 128         |

Objective
To observe how increasing model capacity affects:

- Reconstruction loss
- Quality of reconstructed images
- Structure of latent space

---

### 2️⃣ Variational Autoencoder (VAE)

The same architecture was extended to implement a **Variational Autoencoder**.

Additional Components

- Latent mean vector
- Latent variance vector
- Reparameterization trick
- KL divergence regularization

Purpose
To compare the VAE with the standard autoencoder in terms of:

- Reconstruction performance
- Latent space distribution
- Generative capability

---

## Image Morphing Experiment

A latent space interpolation experiment was conducted.

Procedure:

1. Select an image of digit **0**
2. Select an image of digit **8**
3. Encode both images into latent vectors
4. Interpolate between them with step sizes:

0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9

This generates **nine intermediate images** showing a smooth transition between digits.

This experiment demonstrates how the **latent space captures continuous semantic structure**. 

---

## Model Comparison Goals

The assignment analyzes:
- Impact of **filter size on reconstruction quality**
- Differences between **Autoencoder and VAE latent representations**
- Ability of models to generate **smooth interpolations**
- Relationship between **model capacity and reconstruction loss**

---

## Key Observations
- Increasing convolution filters generally improved reconstruction quality.
- Larger models produced smoother and more structured latent spaces.
- Variational Autoencoders generated more continuous latent representations.
- Latent space interpolation demonstrated meaningful transitions between digits.
- VAEs provided better generative structure compared to standard autoencoders.

---

## Files Included

```
📦 Assignment 3/
│
├── 📄 Assignment_3_Simran_Sinha.ipynb – Implementation of Autoencoder and VAE experiments
│
└── 📘 README.md – Project documentation
```

---

## Conclusion

This assignment demonstrates how generative neural networks learn compressed representations of image data.

While **standard autoencoders focus on reconstruction**, **Variational Autoencoders provide a structured latent space that supports generative tasks and interpolation**.

The experiments show that **architecture design, filter size, and latent space constraints play an important role in generative modeling performance.**


