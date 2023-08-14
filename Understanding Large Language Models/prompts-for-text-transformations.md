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

# 🪵 Prompts for Text Transformations

## Text Transformations

We can perform various kinds of text transformations like language translation, HTML to JSON conversion, spelling correction etc."

**We can perform a variety of text transformations, including:**

* **Language translation:** We can translate text from one language to another. For example, we can translate English text to Spanish or French.
* **HTML to JSON conversion:** We can convert HTML code to JSON format. JSON is a lightweight data-interchange format that is often used for storing and transmitting data.
* **Spelling correction:** We can correct spelling errors in text. This can be helpful for ensuring that text is accurate and professional.

### Get multi Language and multi tonnes&#x20;

```
Translate the following text to Telugu, Hindi, tamil, german, french and italian. tell me both formal and informal tonnes in all languages
'Would you like to learn more?'
```

The response is as&#x20;

```
Telugu
Formal: మరింత తెలుసుకోవాలనుకుంటున్నారా? (Marimta telusukovaalanukuntunnaara?)
Informal: మరింత తెలుసుకోవడానికి ఇష్టపడతారా? (Marimta telusukovadakaniki istupadtara?)
Hindi
Formal: क्या आप और अधिक जानना चाहते हैं? (Kya aap aur adhik jaanana chahte hain?)
Informal: और कुछ जानना चाहते हैं क्या? (Aur kuchh jaanana chahte hain kya?)
Tamil
Formal: மேலும் அறிய விரும்புகிறீர்களா? (Meelum ariya virumpugireenga?)
Informal: இன்னும் கொஞ்சம் தெரிந்துகொள்ள விரும்புகிறீர்களா? (Innum konjam terinthukolva virumpugireenga?)
German
Formal: Möchten Sie mehr erfahren? (Möchten Sie mehr erfahren?)
Informal: Hast du noch Fragen? (Hast du noch Fragen?)
French
Formal: Voulez-vous en savoir plus? (Voulez-vous en savoir plus?)
Informal: Tu veux en savoir plus? (Tu veux en savoir plus?)
Italian
Formal: Vuoi saperne di più? (Vuoi saperne di più?)
Informal: Vuoi sapere altro? (Vuoi sapere altro?)
```

### Get multiple formats

We can convert code from one language to another language

<pre><code><strong>Generate Java equallent of following python code
</strong>
code : ```def hello_world():
  print("Hello, world!")

if __name__ == "__main__":
  hello_world()
```
</code></pre>

The response is as&#x20;

```java
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}

```

### Formal correction and spell check/ Grammar check

We can do spelling and grammar corrections by using large language models
