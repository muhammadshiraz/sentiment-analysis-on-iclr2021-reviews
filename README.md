<p align="center"><img src="images/kocaeli.jpg" width="150"></p>
<h2 align="center">2021 Sentiment Analysis Reviews Project Reports</h2>
<h3 align="center">Muhammad Shiraz</h3>
<p align="center">January 2021</p>
<p align="center">Information Systems Engineering Department</p>
<h3 align="center">KOCAELİ UNIVERSITY</h3>

### Introduction
Sentiment Analysis is the task of identifying whether the opinion expressed in a review is positive or negative or neutral in general, or about a given review. For example: "I love this paper and I think the previous team building strategy behind is worth exploring further" is a general positive text, and the review. and Sentiment Analysis also known as opinion mining refers to the identification, extraction and study of sentiment states by using natural language processing, text analysis, computational linguistics and biometrics.

### Keywords: 
<p>Sentiment Analysis, Reviews, Machine Learning, Supervised Text Classification, Data Visualization.</p>

### Datasets
In this project, we used one dataset. Let us now describe the datasets in more details:
<p align="left">1. ICLR 2020 Conference | OpenReview dataset using selenium crawler</p>
<p align="left">https://openreview.net/group?id=ICLR.cc/2020/Conference</p>
<p align="left">This set is a collection of paper reviews documents labeled with respect to their overall sentiment polarity (positive or negative or neutral). The set collected in 2020-Dec-20 and it contains 702 positive and 794 negative and 1038 neutral processed reviews. The reviews were preprocessed by the dataset editors so that each review is formatted as a plain tokenized text, containing no structured information that can imply on the polarity of the text (e.g., label – 0/1). The average review size (in words) is 40000. Although this set is considered as a user-generated content the language is relatively grammatically correct in most cases, probably because users are not restricted with the size of the text.</p>

<table>
  <tr>
    <th align="left">Review</th>
    <th>Sentiments</th>
  </tr>
  <tr>
    <td>I love this paper and I think the previous team building strategy behind is worth exploring further.</td>
    <td>positive</td>
  </tr>
  <tr>
    <td>The experimental results of the experiment are not made explicitly.</td>
    <td>negative</td>
  </tr>
  <tr>
    <td>This paper can be strengthened by discussion and testing of other forms of distribution in the descriptive family.</td>
    <td>neutral</td>
  </tr>
</table>

### Preprocessing
Before the feature extractor can use the review to build feature vector, the review text goes through preprocessing step where the following steps are taken. These steps convert plain text of the review into processable elements with more information added that can be utilized by feature extractor. For all these steps, third-party tools were used that were specialized to handle unique nature of review text.

### Tokenization
Tokenization is the process of converting text as a string into processable elements called tokens. In the context of a reviews, these elements can be words, emoticons, url links, hashtags or punctuations.

### Train Test Split
To measure the accuracy of the model we are creating, the data needs to split into 2 parts. A training set to fit and tune our model and a testing set to create predictions on and evaluate the model at the very end.

### Classifiers:
We used five different classifiers: RNN, LSTM, kNN, and SVM, ULMFit. Intuitively, the features seem mutually dependent.

### 1: Creating a Linear SVM Model
SVM is a supervised(feed-me) machine learning algorithm that can be used for both classification or regression challenges. Classification is predicting a label/group and Regression is predicting a continuous value. SVM performs classification by finding the hyper-plane that differentiate the classes we plotted in n-dimensional space. SVM draws that hyperplane by transforming our data with the help of mathematical functions called “Kernels”. Types of Kernels are linear, sigmoid, RBF, non-linear, polynomial, etc.,

### 2: Multi-layer Perceptron
MLP is a supervised machine learning algorithm for regression or classification. Within the input and output, there might be some nonlinear layers, called hidden layers. Hence, MLP has the ability to learn nonlinear models. Each of the hidden layers comprises of neurons, which is the number of nodes in the hidden layer. MLP is sensitive to unscaled features, thus it might be important to scale the feature - [0, 1].

### 3: Word2Vec Pre-Trained Embeddings Conversion
Word2vec is a group of related models that are used to produce word embeddings. These models are shallow, two-layer neural networks that are trained to reconstruct linguistic contexts of words. Word2vec takes as its input a large corpus of text and produces a vector space, typically of several hundred dimensions, with each unique word in the corpus being assigned a corresponding vector in the space. Word vectors are positioned in the vector space such that words that share common contexts in the corpus are located in close proximity to one another in the space.

### 4: GloVe Pre-trained Word Embeddings
The training data is not so large, the model might not be able to learn good embeddings for the sentiment analysis. Alternatively, we can load pre-trained word embeddings built on a much larger training data.
The GloVe database contains multiple pre-trained word embeddings, and more specific embeddings trained on tweets. So, this might be useful for the task at hand.
First, we put the word embeddings in a dictionary where the keys are the words and the values the word embeddings.

### 5: ULMFit classification model
ULMFiT, is an architecture and transfer learning method that can be applied to NLP tasks. It involves a 3-layer AWD-LSTM architecture for its representations. The training consists of three steps: 1) general language model pre-training on a Wikipedia-based text, 2) fine-tuning the language model on a target task, and 3) fine-tuning the classifier on the target task.

### 6: Creating model RNN and LSTM
Sentiment Analysis using Recurrent Neural Networks (RNN-LSTM) and Google News Word2Vec.

### Conclusions
In this project we have investigated the task of sentiment analysis as a classification problem. We have used one dataset: iclr2020 paper reviews and reviews statuses that differ mostly in their typical length of each document, and the language style. We believe we have shown that using simple word-based features, it is harder to classify reviews statuses, comparing to iclr2020.
