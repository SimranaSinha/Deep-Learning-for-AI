# IE 7615 – Assignment 2

## Overview

This assignment focuses on sequence modeling for text classification using deep learning architectures.

The task is to implement and compare different neural network models on the Reuters Newswire Classification dataset, analyzing how architectural choices affect classification performance.

The models evaluated include:
	•	SimpleRNN
	•	LSTM
	•	Bidirectional RNN
	•	Feedforward Neural Network (MLP)

---

## Dataset
- Dataset: Reuters Newswire (keras.datasets.reuters)
- Vocabulary size limited to 10,000 words
- Sequences padded/truncated to maximum length of 250 words
- 46 output classes

---

## Preprocessing
- Integer-encoded sequences
- Padding applied to ensure uniform input length
- One-hot encoding for multi-class output
- Train-test split provided by dataset

---

## Models Implemented

1️⃣ SimpleRNN Model

Architecture
	•	Embedding layer (128 dimensions)
	•	SimpleRNN (128 units)
	•	dropout = 0.2
	•	recurrent_dropout = 0.2
	•	Dense output layer (Softmax)

Experiment
	•	Trained with epochs: 5, 10, 15, 20, 25, 30
	•	Observed training and test accuracy trends

Goal
To analyze how increasing epochs affects model performance and overfitting behavior.



2️⃣ LSTM Model

Architecture
	•	Embedding (128)
	•	LSTM (128 units)
	•	dropout = 0.2
	•	recurrent_dropout = 0.2
	•	Flatten layer
	•	Dense output layer

Experiment
	•	Trained for 10 epochs
	•	Compared with best-performing SimpleRNN result


🔹 LSTM + Additional Dense Layer

Modified Architecture
	•	Embedding (128)
	•	LSTM (128)
	•	Dense (128)
	•	Output layer

Purpose
To evaluate whether additional representation learning improves classification accuracy.




3️⃣ Bidirectional SimpleRNN

Architecture
	•	Embedding (128)
	•	Bidirectional SimpleRNN (128 units)
	•	Output layer

Training
	•	10 epochs

Objective
To determine whether using forward and backward context improves classification performance.




4️⃣ Feedforward Neural Network (MLP)

Architecture
	•	Embedding (128)
	•	Flatten
	•	Dense (128)
	•	Dense (128)
	•	Output layer

Training
	•	30 epochs

Objective
To compare a non-recurrent model against sequence-based architectures.

---

## Model Comparison Goals

The assignment evaluates:
-	Impact of recurrent vs non-recurrent architectures
- Effect of long-term memory (LSTM vs SimpleRNN)
- Benefit of bidirectional context
- Effect of model depth
- Influence of training epochs

---

## Key Observations
- SimpleRNN performance improved with epochs but showed signs of saturation.
- LSTM handled long-term dependencies better than SimpleRNN.
- Adding a Dense layer increased representational capacity.
- Bidirectional RNN captured additional contextual information.
- MLP performed competitively but lacked sequential modeling strength.

---

## Files Included

```
📦 Assignment 2/
│
├── 📄 Assignment_Homework_2.ipynb – Full implementation of all models and experiments 
│
└── 📘 README.md - Project documentation

```
---

## Conclusion

This assignment demonstrates how architecture selection directly impacts performance in text classification tasks.

Recurrent models, particularly LSTM and Bidirectional variants, provide stronger sequential understanding compared to basic RNNs and feedforward networks.

Model design, training duration, and architectural depth all play a critical role in classification accuracy.
