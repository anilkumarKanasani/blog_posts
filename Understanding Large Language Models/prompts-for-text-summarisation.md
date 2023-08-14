---
layout:
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

# 🗒 Prompts for Text summarisation

## Text summarization

Text summarization is the process of creating a **brief, accurate**, and informative **summary** of a longer text. It is a type of natural language processing (NLP) task that can be used to extract the key points of a text and present them in a concise and easy-to-understand format.

An example prompt to get text summary is&#x20;

````
Your task is to generate a short summary of a product
review from an ecommerce site. 

Summarize the review below, delimited by triple 
backticks, in at most 15 words. 

Review: ```I ordered my iPhone 14 Pro Max on the day it was released,
and it arrived at my door just two days later! I was very
impressed with the quick delivery time. The phone itself is
amazing, and I'm very happy with my purchase. The price was
a bit high, but I think it's worth it for the quality of the phone.```
````

The response is as&#x20;

```
iPhone 14 Pro Max: Great phone with quick delivery, a bit pricey but worth it.
```

## Summarising in another point of view

We can ask to summarize from shipping point of view as follows

````
Your task is to generate a short summary of a product
review from an ecommerce site to give feedback to shipping department. 

Summarize the review below, delimited by triple 
backticks, in at most 15 words and focusing on any aspects
that mention shipping and delivery of the product. 

Review: ```I ordered my iPhone 14 Pro Max on the day it was released,
and it arrived at my door just two days later! I was very
impressed with the quick delivery time. The phone itself is
amazing, and I'm very happy with my purchase. The price was
a bit high, but I think it's worth it for the quality of the phone.```
````

The response is as&#x20;

```
iPhone 14 Pro Max: Quick delivery, 2 days after release! worth it.
```

Same review to give feedback to product quality department

````
Your task is to generate a short summary of a product
review from an ecommerce site to give feedback to product quality department. 

Summarize the review below, delimited by triple 
backticks, in at most 15 words and focusing on any aspects
that mention about quality of the product. 

Review: ```I ordered my iPhone 14 Pro Max on the day it was released,
and it arrived at my door just two days later! I was very
impressed with the quick delivery time. The phone itself is
amazing, and I'm very happy with my purchase. The price was
a bit high, but I think it's worth it for the quality of the phone.```
````

The response is as&#x20;

```
iPhone 14 Pro Max: Amazing phone, worth the price!
```
