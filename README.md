
## Introduction 🌟

Natural Language Processing (NLP) is a field of artificial intelligence that focuses on the interaction between computers and humans through natural language💬  In this repository, we explore basic NLP tasks using the NLTK (Natural Language Toolkit) library in Python🐍.

![image](https://github.com/ThomasHeim11/NLP-Beginner-Guide/assets/106417552/34aa823d-2200-40d3-8d6e-b8ee44123f16)

📚
In this repository, you'll find code examples that demonstrate various NLP techniques using NLTK. The examples cover the following topics:

- **Segmentation**: Splitting text into sentences.
- **Tokenization**: Breaking sentences into words.
- **Removal of Stop Words**: Removing common words that don't carry much meaning.
- **Stemming and Lemmatization**: Reducing words to their root forms.
- **Part of Speech Tagging**: Tagging each word with its part of speech.
- **Named Entity Recognition**: Identifying named entities like persons, organizations, locations, etc 🌍

  ## Table of Contents 📜

- [Segmentation](#segmentation)✂️
- [Punctuation Removal](#punctuation-removal)✨
- [Tokenization](#tokenization)  🧙‍♂️
- [Removal of Stop Words](#removal-of-stop-words)🔇
- [Stemming and Lemmatization](#stemming-and-lemmatization)🌱
- [Part of Speech Tagging](#part-of-speech-tagging)🏷️
- [Named Entity Recognition](#named-entity-recognition)🌟
- [Examples](#examples)🌠
- [Getting Started](#getting-started)🚀


### Segmentation ✂️

In NLP, breaking text into sentences and words is a common initial step. NLTK provides tools to facilitate this.

```python
import nltk
nltk.download('punkt')
from nltk.tokenize import sent_tokenize, word_tokenize

text = "Millions of people across the UK and beyond have celebrated..."
sentences = sent_tokenize(text)
words = word_tokenize(sentences[2])
print(sentences)
print(words) python
```
### Punctuation Removal✨
Eliminating punctuation is often necessary for various text processing tasks.

```python
import re

text = re.sub(r"[^a-zA-Z0-9]", " ", sentences[2])
print(text)
```
### Tokenization🧙‍♂️
Tokenization involves splitting text into individual words.

```python
from nltk.tokenize import word_tokenize

words = word_tokenize(text)
print(words)
```
### Removal of Stop Words🔇
Stop words are common words frequently removed in NLP analysis.

```python
nltk.download('stopwords')
from nltk.corpus import stopwords

words = [w for w in words if w not in stopwords.words("english")]
print(words)
```

### Stemming and Lemmatization🌱
Stemming and lemmatization are linguistic processes to reduce words to their base forms.

```python
nltk.download('averaged_perceptron_tagger')
pos_tags = nltk.pos_tag(words)
print(pos_tags)
```

### Part of Speech Tagging🏷️
Part of speech tagging involves labeling words with their grammatical attributes.

```python
nltk.download('averaged_perceptron_tagger')
pos_tags = nltk.pos_tag(words)
print(pos_tags)
```
### Named Entity Recognition🌟
Named Entity Recognition (NER) identifies named entities within text.

```python
nltk.download('words')
from nltk import ne_chunk

ner_tree = ne_chunk(pos_tags)
print(ner_tree)
```

### Examples🌠
Here are a few examples showcasing Named Entity Recognition:

```python
text = "Twitter CEO Elon Musk arrived at the Staples Center..."
ner_tree = ne_chunk(pos_tag(word_tokenize(text)))
print(ner_tree)
```

Feel free to explore and expand upon these exercises to deepen your understanding of NLP concepts and NLTK library utilization📚✨

Happy learning!

## Getting Started🚀

To run the code examples in this repository, make sure you have Python and NLTK installed. You can install NLTK using the following command:

```
pip install nltk
```
# Thank you! 🙌

If you appreciated this, feel free to follow!🌟🔮

[![Thomas HeimLinkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thomas-heim11/)
