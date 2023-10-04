---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Transformer architecture

## Text generation before Transformers

Generative algorithms are not new, but previous generations of language models were limited by their reliance on recurrent neural networks (RNNs). RNNs are powerful, but they require a lot of compute and memory to perform well at generative tasks.

## Working of RNN family :-

Recurrent neural networks (RNNs) are a type of neural network that are able to process sequential data. This means that RNNs can take into account the order of inputs, which is important for many tasks such as natural language processing, speech recognition, and machine translation. The family of RNNs are&#x20;

1. Basic RNN
2. LSTM network
3. GRU network
4. Bi-directional LSTM network

### Limitations of RNN family

RNNs are not very good at predicting the next word in a sentence if they only see the previous few words. To make better predictions, RNNs need to see more of the context, such as the whole sentence or even the whole document. However, this can require a lot of resources, and even then the model may not be able to make a perfect prediction.

