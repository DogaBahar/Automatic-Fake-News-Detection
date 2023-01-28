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

_BERT/SBERT dataset_

![bert-data](https://user-images.githubusercontent.com/56762763/215285055-687eb4e3-da2b-439b-aa29-db53d30b078a.png "BERT/SBERT dataset")

_Word2Vec dataset_

![pre-data](https://user-images.githubusercontent.com/56762763/215285148-7e5da3a6-71cd-47a8-8f26-aad4ec9a4641.png)

# Model Selection and Comparision

In this project, I used 3 feature extraction methods to convert my sentences to vectors
and have numerical embeddings. SBERT, BERT and Word2Vec. BERT and SBERT use a
transformer-based architecture, and the pooler_output is the fixed-size representation
of the entire input sentence obtained by applying a pooling operation on the last
hidden state (i.e., the representation of the [CLS] token) of the transformer. This
representation is then used as input to the final classification layer. In summary, BERT
typically generates a multi-dimensional array of hidden states for each input token, a
fixed-dimensional "pooler" output, and the embeddings for each input token.
On these embeddings, I trained them with 4 machine learning classification methods
(KNN, Logistic Regression, Support Vector Machine, and Naive Bayes) after SMOTE
method. For BERT and SBERT classifiers I did not use SMOTE because of not interfere
with their own pipeline process
