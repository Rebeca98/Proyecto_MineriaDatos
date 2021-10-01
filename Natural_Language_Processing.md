Natural Language Processing: how to deal with text data

Natural Language: 
- English
- Chinese
Processing: 
- How computer carries out instructions

1. we can use NLP techniques to do Sentiment Analysis
2. Topic Modeling (Emails labeling)
3. Text Generation 

NLP in Python:
- Programming:
  - Data: pandas, sklearn, re
  - NLP nltk, TextBlob, gensim

- Math and Stats: 
  - Clean: corupus, document-term matrix
  - EDA: word counts
  - NLP: sentiment analysis, topic modeling, text generation
  
- Communication: 
  - Design: scope, visualize, extract insights
  - Domain: expertise

**Data Science Workflow**: 
1. Start with the question
2. Get & Clean the Data
3. perform EDA: usually is donde with visualization techniques
4. Apply Techniques
5. Share Insights

Data Gathering:
 - Web Scrapping:
   - make HTTP requests: get info from a website
 - Beautigul Soup:
   - Parse HTML documents: extract parts of a website
- Saving Python Data: 
  - pickle: serialize python objetcs

**Data**
Different types of analysis requiere different data formats:
1. Corpus: collection of texts
2. Docuemt-Term Matrix: out into a matriz so a machine can learn read it.

¿ How would a computer read? It needs to be cleaned, tokenized and put into matrix

Common **data cleaning** steps: 
- remove punctuation 
- lowercase letters
- remover numbers
(regular experessions: a way to search patterns)

Tokenization: 
split text into smaller pieces (by sentence, by word)
- now that every words is its own token, you can filter out the words that have very little meaning: stop words
- we obtain a 'bag of words model': simple format that ignores order. 

Document-Term Matrix
- each row is a different document
- each row is a different term (words, or bi-grams like "thank you")
- the values are word counts
we can do this using scikit-learn, Count Vectorizer: sklearn way to make a DTM

Exploratory Data Analysis
Input: a corpus and a document-term matrix
EDA: summarize the main characteristics of the data set, often using visual methods
Output: figure out the main trends in the data and if it makes sense. 

Explore:
1. top words: find the most common words for each comedian
    - visualize: word clouds
    - insights: now that you have a bunch of word clouds, you can visually determine a few things:
      - does the data makes sense?
      - can we further clean the data?
      - what are some initial findings?    
2. Vocabulary: take a look at the unique number of words used

NLP Techniques:
Input: clean data
NLP Techniques: advanced analysisis techniques
Output: additional insights about our data to help us answer our question

**TOPIC MODELING**
- INPUT: a document-term matrix. Each topic will consiste of a set of words where order doesn matter, so we are going to start with the bag of words format. }
- gensim: Python toolkit for topic modeling. We are going to use a topic modeling techniue called Latent Dirichlet Allocation and use nltk for some parts-of-speech tagging. It will find the best word distribution for each topic and best topic distribution for each document. 
- Output: the top words in each topic. 

every document consiste of a mix of topics and every topic is a mix of words. 
This is a probabilistic approach to topic modeling. There are also matrix factorization techniques for topic modeling such as Latent Semantic Indexing and Non-negative Matrix Factorization. 

**Text Generation**
Input: A corpus. We want to preserve the order of the text, including punctuation. 
We are going to use Markov Chains to do this, and we can implement this using Python's built-in functions. 
Markov chains are a way of representing how systems change over time. The main concept behind MC are that they are memoryless, meaning that the next state of a process only depends on the previous state. 

- Create a dictionary for a corpus where the keys are the current state and the values are the options for the next state. write a function to randomly generate next terms. 
- This is a oversimplified way of generating text. A much more complex technique would be to use deep learning and Long Short-Term Memory (LSTM).  

Reference: Natural Language Processing in Python, Alice Zhao. github.com/adashofdata
