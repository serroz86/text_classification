# TOPIC MODELING USING WIKIPEDIA ARTICLES

## Goals

Multi-label topic classification using unsupervised learning with python. We use Latent Dirichlet Allocation (LDA) to discover hidden topics from the articles. The source of data to train are +1000000 wikipedia articles from the latest wikipedia dump service. At the end, there is the option to check the output using some text.


## Requirements

a) python 3 and the following modules: xml, codecs, re, os, random, pickle, gensim, nltk, pyLDAvis, matplotlib, math, wordcloud, string, bs4, operator, time

Most of these can be installed using the basic Anaconda installation. 

b) Install the nltk data

There is the option to uncomment the line:
 # nltk.download()

A window will open to ask what nltk data you want to download.

c) It is necessary to download the latest wikipedia pages in form of .xml file, retrieved from https://dumps.wikimedia.org/enwiki/ and place it in the folder "text_classification/".

## Steps

### 1) Preprocess the wikipedia articles

The text from all the wikipedia articles need to be extracted and cleaned (stop words removal, lemmatization, remove symbols...).

### 2) Run the model

We run the LDA model, which creates 50 groups of words (one per topic). The result can be plotted using pyLDAvis https://pyldavis.readthedocs.io/en/latest/ and wordclouds https://www.wordclouds.com/

### 3) Check the results

We (as humans) have to check which words appear in each group, and label that group. Then, it is possible to get the topic of the input text.

## How to run the jupyter notebook

The code can be run by running all the cells in the notebook. 

The main function start with options that are set to True/False. We select whether we want to prepare the database (i.e., extract the wikipedia articles from the xml file), train the model, or check the output with some text examples of wikipedia articles.


```
    prepare_database=False
    train_model=True
    check_result=True
```


