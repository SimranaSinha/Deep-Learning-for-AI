# Deep Learning for AI (IE 7615 - Deep Learning Assignments)

## Overview

This repository contains coursework focused on deep learning model design and performance comparison across image and text classification tasks.

The assignments analyze how architectural choices, model depth, regularization, and training configuration influence classification performance.

---

## Assignment 1 – Fashion MNIST (Image Classification)

This assignment focuses on building and comparing Multi-Layer Perceptron (MLP) and Convolutional Neural Network (CNN) models using the Fashion MNIST dataset.

### Key Areas:
- One vs Two hidden layers in MLP
- 32 , 64, 128, 256 neurons
- 1, 2, 3 Convolutional layers
- Dropout rates: 0.0, 0.1, 0.3, 0.5
- Optimizer comparison: Adam, RMSprop, SGD

### Files Included:

```
📦 Assignment 1/
│
├── 📄 Homework_Assignment_1(Deep_Learning).ipynb
│
└──📘 README.md
```

### Conclusion:
- CNN models outperformed MLP models.
- Increasing model depth improved performance up to a point.
- Dropout reduced overfitting.
- Optimizer choice influenced convergence speed and stability.

---

## Assignment 2 – Reuters Text Classification

This assignment implements and compares sequence modeling architectures on the Reuters Newswire dataset.

### Models Implemented:
- SimpleRNN
- LSTM
- LSTM + Additional Dense Layer
- Bidirectional SimpleRNN
- Feedforward Neural Network (MLP)

### Files Included:

```
📦 Assignment 2/
│
├── 📄 Assignment_Homework_2.ipynb – Full implementation of all models and experiments 
│
└── 📘 README.md - Project documentation
```

### Observations:
- SimpleRNN improved with epochs but showed saturation.
- LSTM handled long-term dependencies better.
- Additional Dense layer increased representational capacity.
- Bidirectional RNN improved contextual understanding.
- MLP performed competitively but lacked sequential modeling strength.

---

Assignment 3 – Autoencoder & Variational Autoencoder (MNIST)
This assignment explores generative representation learning using Autoencoders and Variational Autoencoders on the MNIST handwritten digit dataset. The goal is to analyze reconstruction quality, latent space structure, and the effect of model capacity.

Models Implemented:
- Convolutional Autoencoder
- Variational Autoencoder (VAE)
- Autoencoder with different filter configurations
- Latent Space Interpolation (Digit Morphing)

Files Included:

```
📦 Assignment 3/
│
├── 📄 Assignment_3_Simran_Sinha.ipynb – Implementation of Autoencoder and VAE experiments
│
└── 📘 README.md – Project documentation
```

Observations:
- Increasing convolution filters improved reconstruction quality.
- Variational Autoencoder produced smoother latent space distributions.
- Latent space interpolation successfully generated gradual transitions between digits.
- Higher model capacity reduced reconstruction loss but increased complexity.

---

## Conclusion

These assignments demonstrate that architecture selection, training duration, and regularization strategies directly impact deep learning model performance across image and text classification tasks.
