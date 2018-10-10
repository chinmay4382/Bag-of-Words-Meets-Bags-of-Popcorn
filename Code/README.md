# Kaggle: Bag of Words Meets Bags of Popcorn
This is a solution for the Kaggle Data Science competition "Bag of Words Meets Bags of Popcorn"

https://www.kaggle.com/c/word2vec-nlp-tutorial

## Description
By learning from a list of already classified movie reviews, the algorithm needs to predict if a new one is either positive or 
negative. 

### Dependencies
- pandas &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; pip3 install pandas
- numpy &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;pip3 install numpy
- BeautifulSoup4 &nbsp; pip3 install bs4
- nltk &nbsp; &nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp; &nbsp; pip3 install nltk [Details](http://www.nltk.org/install.html)
- gensim &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; pip3 install gensim
- sklearn &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; pip3 install sklearn


### Preprocessing

- 1.Remove HTML using "BeautifulSoup4"
- 2.Remove non-letters using "re" 
- 3.Convert to lower case, split into individual words using inbuilt methods ".lower()" and ".split()"
- 4.Remove stop words :These are frequently occurring words that don't carry much meaning [Details](https://en.wikipedia.org/wiki/Stop_words)

### Creating Features from a Bag of Words (Using scikit-learn) (bow.ipynb)

The Bag of Words model learns a vocabulary from all of the documents, then models each document by counting the number of times 
each word appears. For example, consider the following two sentences:

In the IMDB data, we have a very large number of reviews, which will give us a large vocabulary. To limit the size of the feature
vectors, we should choose some maximum vocabulary size. Below, we use the 5000 most frequent words 
(remembering that stop words have already been removed)

### Model fitting

It does two functions: 
**First,** it fits the model and learns the vocabulary; 
**Second,** it transforms our training data into feature vectors.


### [Multilayer Perceptron](https://en.wikipedia.org/wiki/Multilayer_perceptron)

A multilayer perceptron (MLP) is a class of [feedforward](https://en.wikipedia.org/wiki/Feedforward_neural_network) [artificial 
neural network](https://en.wikipedia.org/wiki/Artificial_neural_network). An MLP consists of, at least, three layers of nodes: 
an input layer, a hidden layer and an output layer. Except for the input nodes, each node is a neuron that uses a nonlinear 
activation function. MLP utilizes a [supervised learning](https://en.wikipedia.org/wiki/Supervised_learning) technique called 
[backpropagation](https://en.wikipedia.org/wiki/Backpropagation) for training.Its multiple layers and non-linear activation 
distinguish MLP from a linear perceptron. It can distinguish data that is not linearly separable


### Prediction

To predict the output of test data we use use the above built classifier on test data i.e testData.tsv. Here only "transform",
is called not "fit_transform" as did for the training set. In machine learning, if fit command is used on test data then
there is risk of overfitting. 

Overfitting is a process in which the model tends to memorise the train data and hence fail in predicting unseen data that
results in failure of model built.




