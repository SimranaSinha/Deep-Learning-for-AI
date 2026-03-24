# Assignment 4 – Transformers for Text Generation and Classification

**IE 7615 – Deep Learning for AI**

## Overview

This assignment focuses on implementing Transformer architectures for two different NLP tasks:

1. Recipe text generation using a Transformer language model
2. Sentiment classification using a Transformer model on the IMDB dataset

The goal is to understand how Transformers perform compared to traditional LSTM models for sequence modeling tasks such as text generation and text classification. 

---

## Tasks Implemented

### Part I – Recipe Generation using Transformer

* Modified the Transformer model to generate recipes
* Trained model on Epicurious Recipe Dataset
* Generated recipes using different temperature values
* Compared generated recipes with LSTM autoregressive model outputs
* Analyzed:

  * Coherence
  * Creativity
  * Diversity of generated recipes

### Part II – Sentiment Classification using Transformer

* Adapted Transformer model for binary text classification
* Used IMDB movie review dataset
* Trained and evaluated Transformer model
* Compared performance with LSTM-based sentiment classifier
* Analyzed performance differences based on model architecture and long-range dependency learning

---

## Model Parameters Used

The following parameters were used for both Transformer models:

* VOCAB_SIZE = 10000
* MAX_LEN = 200
* EMBEDDING_DIM = 100
* N_UNITS = 128
* BATCH_SIZE = 32
* EPOCHS = 20
* VALIDATION_SPLIT = 0.2
* SEED = 42

---

## Files Included

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

---

## Observations

### Recipe Generation (Transformer vs LSTM)

* Transformer generated more diverse text compared to LSTM
* Higher temperature increased creativity but reduced coherence
* Lower temperature produced more structured recipes
* LSTM outputs were more repetitive but more stable

### Sentiment Classification

* Transformer performed competitively with LSTM
* Transformer handled long sequences better due to attention mechanism
* Training time was higher for Transformer compared to LSTM
* Transformers capture long-range dependencies more effectively

---

## Conclusion

This assignment demonstrated the effectiveness of Transformer models for both text generation and text classification tasks. Transformers performed well in handling long-range dependencies and produced more diverse text generation compared to LSTM models. However, they require more computational resources and training time.

