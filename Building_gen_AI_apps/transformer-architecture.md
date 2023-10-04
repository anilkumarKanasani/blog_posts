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

# ☠ Transformer architecture

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

In the below example, the word great is predicted based on previous three words. But it is not correct prediction when we considered the total sentense.

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Language is more complex. Almost every word has various meanings and its context is very import to derive the meaning of the word.

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

To over come all the limitations, In 2017, the publication of the paper "Attention Is All You Need" by Google and the University of Toronto revolutionized the field of generative AI. The transformer architecture, which was introduced in this paper, has enabled the progress that we see in generative AI today. These are able to generate more coherent and informative text, translate languages more accurately, and perform other generative tasks more effectively.

## Transformer architecture

