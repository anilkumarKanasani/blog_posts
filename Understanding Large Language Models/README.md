---
cover: .gitbook/assets/Screenshot 2023-08-15 at 10.13.41 AM.png
coverY: -2.167664670658681
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# 👋 Introduction

{% hint style="info" %}
**Acknowledgement :**&#x20;

I would like to express my sincere gratitude to my instructors, [Isa Fulford](https://www.linkedin.com/in/isabella-fulford/) from [OpenAI](https://openai.com/) and [Andrew Ng](https://www.linkedin.com/in/andrewyng/) from [DeepLearning AI](https://www.deeplearning.ai/), for their guidance and support in helping me to learn about large language models. I gained most of the knowledge to write this blog post from their lectures and tutorials.

I would also like to thank the [Bard tool ](https://bard.google.com/)for generating the text for this blog post. I am grateful for the opportunity to use Bard and to learn about large language models.



I hope this blog post is informative and helpful.
{% endhint %}

## Introduction

**Large language model (LLM) web interfaces are powerful tools that can be used for a variety of tasks.** These interfaces allow users to interact with LLMs through a web browser, making them accessible to a wide range of people.

LLMs can be used for a variety of tasks, including:

* Text summarisation: LLMs can be used to summarise long pieces of text into shorter, more concise versions. This can be helpful for students, researchers, and anyone else who needs to quickly read and understand large amounts of text.
* Question answering: LLMs can be used to answer questions about a variety of topics. This can be helpful for students, researchers, and anyone else who needs to quickly find information.
* Creative text generation: LLMs can be used to generate creative text formats, such as poems, code, scripts, musical pieces, email, letters, etc. This can be helpful for artists, writers, and anyone else who wants to create new and interesting content.

Under the hood, LLM web interfaces **send API calls to LLM servers**. These servers are responsible for processing the user's requests and generating the output.

Some of the most well-known LLMs in the open source community include:

* [OpenAI ChatGPT](https://openai.com/chatgpt)
* [Google Bard](https://blog.google/technology/ai/bard-google-ai-search-updates/)
* [Facebook LLAMA](https://research.facebook.com/publications/llama-open-and-efficient-foundation-language-models/)

These LLMs are constantly being improved, and new ones are being developed all the time. As LLMs become more powerful, they will become even more useful tools for a variety of tasks.

**The content of API calls is critical for any application.** The instructions that are sent in API calls are called **prompts**. In this blog post, we will discuss in detail how to write prompts for various types of use cases.

**Prompts are important because they determine the output of the API call.** If the prompt is not clear or concise, the API call may not return the desired results. It is important to carefully consider the purpose of the API call and the desired output when writing the prompt.

The prompts should be very clear, specific and concise to the required task to be done by the model.&#x20;

## Types of Large Language Models

On the higher level, any type of LLMs can be divided into one of the two following categories.

1. [Base LLM](./#base-llm)
2. [(Instruction) fine-tunned LLM](./#fine-tunned-llms)

### Base LLM

**Base LLM models** are trained on massive amounts of text data from the internet. Usually, the corpus  of text is collected by web scrapping all the open sourced text based websites like wikipedia. This data can include books, articles, websites, and social media posts. The model learns to predict the most likely next word (or sequence of words) based on a given sequence of text input.

For example, if an end user entered the following text as input:

> <mark style="color:green;">The world is a very different place</mark>

The base LLM model could write the possible next words to the given text. The output could be something like:

> <mark style="color:green;">The world is a very different place</mark> <mark style="color:orange;">than it was just 20 year's ago. Climate change has caused wide spread devastation. And many major cities have been abandoned.</mark>

However, base LLM models are not useful for answering questions from end users. For example, if an end user asked the following question to a base LLM model:

> <mark style="color:green;">What is the longest river in the world?</mark>

Then the base model might give the following replies.

> <mark style="color:green;">What is the longest river in the world?</mark>&#x20;
>
> <mark style="color:orange;">What is the highest mountain in the world?</mark>&#x20;
>
> <mark style="color:orange;">What is the most populist country in the world?</mark>

This is because base LLM models are not trained on question-answering data. They are only trained to predict the possible next word, so they do not have the knowledge or understanding to answer questions correctly.

### Fine-tunned LLMs

To address this limitation, researchers have developed **fine-tuned LLMs**. Fine-tuned LLMs are trained on a combination of text data and **prompts**. Prompts are instructions that tell the LLM what to do. For example, if an end user asks the following question to a fine-tuned LLM:

> <mark style="background-color:green;">( prompt :- Please give answer to a given question )</mark>
>
> <mark style="color:green;">What is the longest river in the world?</mark>

The prompt tells the LLM that the user is looking for the answer to a specific question. The LLM can then use its knowledge of the world to provide an accurate and informative answer. In this case, the LLM would most likely answer with the

> <mark style="color:orange;">Nile River</mark>

**Fine-tuned LLMs are typically developed by first training a base LLM on a massive dataset of text.** The base LLM is then fine-tuned on a smaller dataset of text that includes instructions. The instructions tell the LLM what to do, such as answer questions or summarising text etc.

This process of fine-tuning allows the LLM to learn the relationships between words and the instructions. This, in turn, allows the LLM to give better attempts at following those instructions. Instruction based Fine-tunned LLMs have the potential to revolutionise the way we interact with NLP models.

Feedback is typically collected using [reinforcement learning with human feedback](https://en.wikipedia.org/wiki/Reinforcement\_learning\_from\_human\_feedback) (RLHF). RLHF is a technique that allows an LLM to learn from human feedback.

The quality of the answer from an LLM (or from any person in general) depends on the quality of the question. A well-defined and informative question will yield a more valuable answer than a poorly defined or ambiguous question. In the following sections, we will discuss the [principles of writing effective questions for LLMs](broken-reference).

