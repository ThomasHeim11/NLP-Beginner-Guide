# Natural Language Processing with NLTK

This repository contains code examples and exercises for beginners to learn Natural Language Processing (NLP) using Python and the Natural Language Toolkit (NLTK) library.

## Introduction

Natural Language Processing (NLP) is a field of artificial intelligence that focuses on the interaction between computers and humans through natural language. In this repository, we explore basic NLP tasks using the NLTK (Natural Language Toolkit) library in Python.

In this repository, you'll find code examples that demonstrate various NLP techniques using NLTK. The examples cover the following topics:

- **Segmentation**: Splitting text into sentences.
- **Tokenization**: Breaking sentences into words.
- **Removal of Stop Words**: Removing common words that don't carry much meaning.
- **Stemming and Lemmatization**: Reducing words to their root forms.
- **Part of Speech Tagging**: Tagging each word with its part of speech.
- **Named Entity Recognition**: Identifying named entities like persons, organizations, locations, etc.


## Example Code

Here's an example of the code included in this repository:

```python
# Import NLTK and download necessary resources
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
nltk.download('maxent_ne_chunker')
nltk.download('words')

from nltk.tokenize import sent_tokenize, word_tokenize
from nltk.corpus import stopwords
from nltk.stem.porter import PorterStemmer
from nltk.stem.wordnet import WordNetLemmatizer
from nltk import pos_tag, ne_chunk

# Example text
text = "Millions of people across the UK and beyond have celebrated the coronation of King Charles III..."

# Sentence segmentation
sentences = sent_tokenize(text)

# Word tokenization
words = word_tokenize(sentences[2])

# Remove punctuation and lowercase
words = [w.lower() for w in words if w.isalnum()]

# Remove stopwords
words = [w for w in words if w not in stopwords.words("english")]

# Stemming
stemmed = [PorterStemmer().stem(w) for w in words]

# Lemmatization
lemmatized = [WordNetLemmatizer().lemmatize(w) for w in words]

# Part of speech tagging
pos_tags = pos_tag(words)

# Named Entity Recognition
ner_tree = ne_chunk(pos_tags)

print("Original text:", text)
print("Sentences:", sentences)
print("Tokenized words:", words)
print("Stemmed words:", stemmed)
print("Lemmatized words:", lemmatized)
print("Part of speech tagging:", pos_tags)
print("Named Entity Recognition:", ner_tree)
'''


## Getting Started

To run the code examples in this repository, make sure you have Python and NLTK installed. You can install NLTK using the following command:

'''pip install nltk''
