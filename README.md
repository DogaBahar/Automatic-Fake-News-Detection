# Automatic-Fake-News-Detection
This project aims to use several Machine Learning Algorithms to choose the best-performing model that can classify news as fake or true, by using Natural Language Processing techniques for textual analysis.

# Methods
A news dataset was specially selected inthe Turkish language to contribute to the Turkish 
literature studies in the field of NLP. This process contains the Tokenization and Vectorization
of the dataset using Word2Vec, BERT(Bidirectional Encoder Representations from Transformers) and
SBERT(Sentence-BERT) Feature Extraction methods, classification with Machine Learning Models such
as Support Vector Machine, Naive Bayes, Logistic Regression, KNN(K Nearest Neighbors) and deep 
learning methods BERT/SBERT classifier.

# Introduction
To prevent the spread of fake news on social platforms and make them safer, many
disciplines along with computer science have started to take an action. Especially in
the English language with the help of many datasets, there have been very successful
experiments. The motivation is to improve the conducting studies for also
Turkish Language with Turkish dataset. Along with Natural Language Processing
(NLP) solutions also Machine Learning (ML) models has taken a big part to make
binary classification such algorithms as Logistic Regression, Support Vector Machines,
Naive Bayes, KNN etc. In this project these models are used in order to find the best
result.

## Challanges

* The limited availability of Turkish Language Fake news datasets.
* The imbalance of the fake and true data.
* Including the punctuation in the texts.
* The length unbalance of True and Fake news text

# Corpus Creation
In this dataset 3 main resources have been used:

* Global open source GDELT Project
* Data resource from teyit.org
* Fake news resource from zaytung.com

However in this dataset the gap between true and fake news were so huge. SMOTE (Synthetic
Minority Oversampling Technique) solution is used to overcome the difference with following 
modifications: 

First of all I randomly selected only 20.000 True news
and with web scrawling methods I increased the fake data to 5.157 from teyit.org and
Turkish fake news source zaytung.com. After preparing the dataset, to make it useful and to utilize some pre-processing
steps must be done. For feature extraction, vectorization of the words is done with
Word2Vec, BERT and SBERT. To make it function better for Word2Vec, HTML Tags
are removed, specail characters are removed, all punctuation are removed, Turkish
stop words are removed, all words converted to lowercase and stemming is done with
Turkish stemming library Zemberek. For BERT classifier punctuation were not
removed and no stemming has done, only special characters, Turkish stop words and
HTML tags were removed. 

