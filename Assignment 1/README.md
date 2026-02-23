# IE 7615 – Assignment 1

## Overview

This assignment focuses on building and comparing Multi-Layer Perceptron (MLP) and Convolutional Neural Network (CNN) models using the Fashion MNIST dataset.

The goal is to analyze how different architectures, dropout rates, and optimizers affect classification performance.

---

## Dataset
- Dataset: Fashion MNIST (keras.datasets.fashion_mnist)
- 60,000 training images
- 10,000 test images
- Image size: 28 × 28 grayscale
- 10 output classes

---

## Preprocessing
- Normalized pixel values to range [0,1]
- Flattened images for MLP (784 features)
- Reshaped images to 28×28×1 for CNN
- One-hot encoding for output labels

---

## Part 1 – Multi-Layer Perceptron (Dense Networks)

Objective

Compare:
	•	One hidden layer vs Two hidden layers
	•	32, 64, 128, 256 neurons per layer

Architecture
	•	Dense hidden layers (ReLU activation)
	•	Output layer (Softmax)

Goal

Identify the best model based on:
	•	Accuracy
	•	Robustness
	•	Number of parameters

---

## Part 2 – Convolutional Neural Networks

A. Effect of Convolutional Layers

Tested:
	•	1 Conv layer (128 filters)
	•	2 Conv layers (64 → 128 filters)
	•	3 Conv layers (32 → 64 → 128 filters)

All used:
	•	3×3 filters
	•	One Dense layer before output

---

B. Effect of Dropout

Added dropout after:
	•	Each convolutional layer
	•	Dense layer

Tested dropout rates:
	•	0.0
	•	0.1
	•	0.3
	•	0.5
---

C. Effect of Optimizers

Compared:
	•	Adam
	•	RMSprop
	•	SGD

---

## Final Comparison

Compared:
	•	Best MLP model
	•	Best CNN model

Evaluation based on:
	•	Test accuracy
	•	Generalization performance
	•	Model complexity

---

## Files Included

```
📦 Assignment 1/
│
├── 📄 Homework_Assignment_1(Deep_Learning).ipynb
│
└── README.md
```
---

## Conclusion

- CNN models outperformed MLP models due to better spatial feature extraction.
- Increasing model depth improved performance up to a point.
- Dropout helped reduce overfitting when properly tuned.
- Optimizer choice influenced convergence speed and stability.

This assignment demonstrates how architecture design directly impacts image classification performance.
