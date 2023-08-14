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

# 🐒 Prompts for Text analysis

## Text analysis

We can perform various kinds of text analysis to get more in depth details of given piece of text." Here are some examples of text analysis that can be performed:

* **Sentiment analysis:** This type of text analysis can be used to determine the overall sentiment of a piece of text, such as whether it is positive, negative, or neutral.
* **Topic modeling:** This type of text analysis can be used to identify the main topics that are discussed in a piece of text.
* **Entity extraction:** This type of text analysis can be used to identify the important entities that are mentioned in a piece of text, such as people, places, and organisations.
* **Keyphrase extraction:** This type of text analysis can be used to identify the most important keywords in a piece of text.
* **Text summarization:** This type of text analysis can be used to create a brief summary of a longer piece of text.

These are just a few examples of the many different kinds of text analysis that can be performed. By performing these types of analysis, we can gain a deeper understanding of the meaning and structure of text data.

### Get sentiment

```
What is the sentiment of the following product review, 
which is delimited with triple backticks?

Review text: '''I ordered my Bose QuietComfort 45 from Bose's website,
and it took over a week to arrive at my door! I was very disappointed
with the long delivery time. The headphones themselves are okay
but the noise cancellation is not as good as the previous generation.
I'm not very happy with my purchase, and I would not recommend them to anyone.'''
```

The response is as&#x20;

```
The sentiment of the product review is negative.
```

### Get emotions

We can extract to emotions from a given piece of text

<pre><code><strong>Identify a list of emotions that the writer of the
</strong>following review is expressing. Include no more than
five items in the list. Format your answer as a list of
lower-case words separated by commas.

Review: ```I ordered my Bose QuietComfort 45 from Bose's website,
and it took over a week to arrive at my door! I was very disappointed
with the long delivery time. The headphones themselves are okay
but the noise cancellation is not as good as the previous generation.
I'm not very happy with my purchase, and I would not recommend them to anyone.```
</code></pre>

The response is as&#x20;

```
disappointed, irritated, unsatisfied, unhappy, frustrated
```

### Get Entities

We can extract to entities from a given piece of text

````
Identify the following items from the review text: 
- Item purchased by reviewer
- Company that made the item

The review is delimited with triple backticks.
Format your response as a JSON object with
"Item" and "Brand" as the keys. 
If the information isn't present, use "unknown"
as the value.
Make your response as short as possible.

Review: ```I ordered my Bose QuietComfort 45 from Bose's website,
and it took over a week to arrive at my door! I was very disappointed
with the long delivery time. The headphones themselves are okay
but the noise cancellation is not as good as the previous generation.
I'm not very happy with my purchase, and I would not recommend them to anyone.```
````

The response is as&#x20;

```
{
  "Item": "Bose QuietComfort 45 Headphones",
  "Brand": "Bose"
}
```

### Multi tasking

It is possible to perform all of the tasks listed above in a single prompt. However, it is important to provide a detailed description of the prompt to ensure that the model is able to correctly execute the tasks.
