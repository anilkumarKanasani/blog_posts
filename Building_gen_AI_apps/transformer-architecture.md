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

***

## Transformer architecture

The transformer architecture's strength lies in its capacity to understand the significance and context of every word in a sentence, not just in relation to its immediate neighbours, but with respect to every other word in the sentence. This is achieved by using attention weights to determine how relevant each word is to all other words, regardless of their position in the input.

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

### Self-attention

The provided diagram, referred to as an attention map, effectively visualizes the attention weights that link each word to every other word in a sentence. Notably, the word "book" exhibits a strong connection or attention towards both "teacher" and "student." This phenomenon is termed self-attention, and the model's capacity to acquire such intricate relationships across the entire input greatly enhances its language encoding capabilities.

<figure><img src="https://lh4.googleusercontent.com/1cUBomIW_ZR9DSboT-VXyBbT3OnNFM6dLH5b77cZBwRrpdY2Ck40yGeNPvELQPeXqGmDU3bFgVYWh4tdyDdqbbbbXa39KMmM5S8L5fn0lrj7fv25h3jZt7uDkHOguAOW4VTvB7N6eunW5ZGg_nZs_94" alt=""><figcaption></figcaption></figure>

### Hight level overview of architecture

The central element in the entire architecture is the self-attention layer, although there are several other components apart from it. The transformer architecture is divided into two main parts: the encoder and the decoder, which collaborate closely and exhibit certain commonalities. Inputs are positioned at the bottom, while outputs are located at the top of the model. It's important to note that machine learning models operate with numerical data, not textual content, requiring the conversion of input text into numerical representations.&#x20;

<figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

All the components in the architecture are described as follows.

### Tokenizer

Text is transformed into numerical representations through tokenization, where each number corresponds to a specific position within a dictionary containing all possible words the model can process. Tokenizers come in various types, some converting whole words into numbers while others break down words into smaller pieces for numerical encoding. It's crucial to maintain consistency by using the same tokenizer when generating text.

<figure><img src="https://lh5.googleusercontent.com/--dcLzgPmbe5caKCvpyJ-oXc5tlmdeuoKeVbAZLDmSZG90Vx7MM5OD-PC3_z6WsXv6XPEC2HqfySktoffaD4pD4kxUoejljwIB1D7M3wAike56zeJKP6Y8pgDPA2M65_AnjTkM-vjDaL_xkO3YD-eZc" alt=""><figcaption></figcaption></figure>

### Embedding Layer&#x20;

This layer serves as a trainable vector embedding space, where tokens are represented as unique vectors in a high-dimensional space. Each token in the vocabulary is associated with a multi-dimensional vector, enabling the encoding of meaning and context for individual tokens within the input sequence. Examples of embedding models include word2vec and Doc2Vec. In the paper, tokens were transformed into 512-dimensional vectors.

<figure><img src="https://lh6.googleusercontent.com/O1n9QOj7lwoCuiDotGIOjDv_kxZsfphlrMNL-thpQ80YrFQOoGKrVzsLI50JcJ29MiX7H0TtXOFOfZi9ThnEJ3nw2eYdb0KKVIcg1nkE3tfyvjOU-OuScifuF6V6SjbhYks6u0AdGS6e0QHRszTOUto" alt=""><figcaption></figcaption></figure>

By visualizing words in a three-dimensional vector space, it becomes apparent how their relationships can be depicted. Words located closely to each other in this embedding space are related, and their distance can be calculated as an angle. This mathematical approach enables the model to gain a deeper understanding of language.

<figure><img src="https://lh5.googleusercontent.com/7nM8vQKRFzYTCT8mjjixrPEnjsP3fRX1JyfGUjhVr-O0mSEUkqbqnDZd_OFwa1mKxFvmIZuEg5Q0auNSaNxWm0CP9RJAT9mtb2calxzgKlYgQv85K8RSffaP3yRoRSdVJzcQClVV3pKgcGdzYWFeXrQ" alt=""><figcaption></figcaption></figure>

### Positional Encoding&#x20;

In the encoder or decoder, token vectors are incorporated along with positional encoding to maintain information about word order. This ensures that the model processes input tokens in parallel without losing the significance of each word's position in the sentence.

<figure><img src=".gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### Multi Head self attention

In this context, the model examines the connections among tokens in the input sequence, allowing it to emphasize different parts of the sequence for a more comprehensive understanding of word relationships. The self-attention mechanism in transformer architecture involves multiple independent self-attention heads, with the number varying across models (typically between 12-100). Each self-attention head learns a different facet of language, such as relationships between entities, sentence activities, or rhyming words. Importantly, the specific aspects of language learned by each attention head are not predetermined but emerge through random initialization and extensive training. While some attention maps are easily interpretable, others may be more complex.

<figure><img src=".gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### Softmax layer

The output of feed forward layer consists of logits, which are proportional to the probability scores for every token in the tokenizer dictionary. These logits can be further processed through a softmax layer to normalize them into probability scores for each word. The resulting output provides a probability score for every word in the vocabulary, often comprising thousands of scores. Among these scores, one token will typically have the highest value, representing the most likely predicted token.

<figure><img src=".gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

### Softmax layer

If you want to learn more about working of transformer models, I recommend to go through the following page

{% embed url="http://jalammar.github.io/illustrated-transformer/" %}

{% embed url="https://www.youtube.com/watch?v=-QH8fRhqFHM" %}
