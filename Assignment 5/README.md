# Assignment 5 - Generative Models (RealNVP & Energy-Based Models)

## Overview

This assignment focuses on generative modeling using **Normalizing Flows (RealNVP)** for density estimation and **Energy-Based Models (EBM)** for image generation. The objective is to understand probabilistic generative models, training behavior, and how model parameters affect generated samples and density estimation quality.

The assignment is divided into two parts:

1. Density Estimation using RealNVP
2. Energy-Based Model using Fashion-MNIST

The tasks involve training models with different parameters, comparing training and validation loss, and analyzing generated samples and density estimation results. 

---
## Part 1 – Density Estimation using RealNVP

In this part, the RealNVP normalizing flow model is used for density estimation on a synthetic dataset.

### Dataset

* Two circles dataset generated using `make_circles`
* 30,000 samples
* factor = 0.5
* noise = 0.05

### Experiments Performed

The model was trained with different epoch values:

* 10 epochs
* 50 epochs
* 100 epochs
* 200 epochs
* 300 epochs

Additionally, the number of coupling layers was varied to observe the effect on density estimation:

* 2 coupling layers
* 4 coupling layers
* 8 coupling layers
* 16 coupling layers
* 32 coupling layers

### Observations

* Increasing epochs improved density estimation and reduced loss.
* Increasing coupling layers improved model flexibility.
* Too many coupling layers increased training complexity.
* Model gradually learned the circular distribution.

---

## Part 2 – Energy-Based Model (Fashion-MNIST)

In this part, an Energy-Based Model was trained on the Fashion-MNIST dataset to generate images using Langevin dynamics.

### Dataset

* Fashion-MNIST
* Images resized to 32×32
* Grayscale images

### Model Parameters Used

* IMAGE_SIZE = 32
* CHANNELS = 1
* STEP_SIZE = 10
* STEPS = 60
* NOISE = 0.005
* ALPHA = 0.1
* GRADIENT_CLIP = 0.03
* BATCH_SIZE = 128
* BUFFER_SIZE = 8192
* LEARNING_RATE = 0.0001
* EPOCHS = 60

### Experiments

Images were generated using different step sizes:

* step_size = 5
* step_size = 10
* step_size = 20
* step_size = 50
* step_size = 100

### Observations

* Small step size produced smoother images but slower convergence.
* Medium step size generated better image quality.
* Large step size produced noisy or distorted images.
* Step size significantly affects image generation quality in Energy-Based Models.

---

## Files Included

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

---


## Key Learning Outcomes

* Understanding density estimation using Normalizing Flows.
* Understanding invertible transformations in RealNVP.
* Training Energy-Based Models using Langevin dynamics.
* Effect of epochs and coupling layers in RealNVP.
* Effect of step size in Energy-Based image generation.
* Comparison of training and validation loss behavior.
* Understanding generative modeling techniques.

---

## Conclusion

This assignment demonstrated generative modeling using Normalizing Flows and Energy-Based Models. RealNVP successfully learned the density distribution of the synthetic dataset, and the Energy-Based Model was able to generate Fashion-MNIST images using Langevin dynamics. The experiments showed that model parameters such as epochs, coupling layers, and step size significantly affect model performance and generated output quality.

