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

## Assignment 3 – Autoencoder & Variational Autoencoder (MNIST)
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

## Assignment 4 – Sequence Models (Transformers vs LSTM)

This assignment focuses on sequence modeling and compares Transformer models with LSTM networks for sequence prediction tasks. The goal is to understand how attention-based models perform compared to recurrent neural networks.

### Key Areas:

* Transformer architecture
* LSTM sequence modeling
* Training and validation loss comparison
* Effect of temperature parameter
* Transformer vs LSTM performance comparison

### Files Included:

```
📦 Assignment 4/
│
├── 📄 Assignment_4_Deep_Learning.ipynb    – Full implementation
│
├── 📄 transformer_imdb_model.keras        – Saved Transformer sentiment model
│
├── 📄 final_recipe_transformer.weights.h5 – Recipe generation model weights
│
└── 📘 README.md                           – Project documentation
```

### Conclusion:

* Transformers performed better for long sequence dependencies.
* LSTM performed well but training was slower.
* Transformer loss decreased faster than LSTM.
* Temperature parameter affected sequence generation diversity.

---

## Assignment 5 – Generative Models (RealNVP & Energy-Based Models)

This assignment focuses on generative models including Normalizing Flows (RealNVP) for density estimation and Energy-Based Models for image generation using Fashion-MNIST.

### Key Areas:

* RealNVP density estimation
* Effect of epochs on training loss
* Effect of coupling layers
* Energy-Based Model training
* Image generation using Langevin dynamics
* Step size effect on generated images

### Files Included:

```
📦 Assignment 5/
│
├── 📄 Assignment_5_NNDL.ipynb                               – Implementation of RealNVP and Energy-Based Model
│
├── 🗂️ Output/
│   │
│   ├── 🎞️ Density for each coupling layer count.png
│   │
│   ├── 🎞️ Density for each epoch run.png
│   │
│   ├── 🎞️ EBM – Training & Validation Loss (Fashion MNIST).png
│   │
│   ├── 🎞️ Task 2 – Loss Curves (num_coupling_layers = 8).png
│   │
│   └── 🎞️  Task 3 – Loss Curves (Epochs = 100).png
│
└── 📘 README.md                                            – Project documentation
```

### Conclusion:

* Increasing epochs improved density estimation in RealNVP.
* More coupling layers improved model flexibility.
* Energy-Based Models successfully generated Fashion-MNIST images.
* Step size significantly affected image quality and stability.

---

If you want, I can also make **Assignment 2, 3, 4, 5 all short READMEs in same format** so your whole repo looks consistent.


## Conclusion

These assignments demonstrate that architecture selection, training duration, and regularization strategies directly impact deep learning model performance across image and text classification tasks.
