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


### [Random Forest](http://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

(Random Forest uses many tree-based classifiers to make predictions, hence the "forest"). Below, we set the number of trees to 100 as a reasonable default value. More trees may (or may not) perform better, but will certainly take longer to run. Likewise, the more features you include for each review, the longer this will take.

The classifier("forest") is built which can be further used to predict the sentiment of the data(test)

### Prediction

To predict the output of test data we use use the above built classifier on test data i.e testData.tsv. Here we only call 
"transform", not "fit_transform" as we did for the training set. In machine learning, you shouldn't use the test set to fit your
model, otherwise you run the risk of overfitting. 



