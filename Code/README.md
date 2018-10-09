# Kaggle-Word2vec
Solution for the Kaggle Data Science competition "Bag of Words Meets Bags of Popcorn"

https://www.kaggle.com/c/word2vec-nlp-tutorial

##Description
By learning from a list of already classified movie reviews, the algorithm needs to predict if a new one is either positive or negative. 

##Solution

###Input

####Labeled reviews
data/labeledTrainData.tsv

####Unlabeled reviews
data/unlabeledTrainData.tsv

###Parser
For both labeled and unlabeled reviews:
* Preserve relevant text
* Hashing trick (dimensions, wrapped words)

###Training and Clasification

####Algorithms:
* Naive Bayes
* Perceptron

####Steps
For each algorithm:

1) Train with labeled reviews

2) Clasify unlabeled reviews (give probability based on previous learning)

3) Define weight

Then, for each unlabeled review:

1) Calculate the normalized resulting probability based on weights 

2) Round probability to 0 or 1 (Negative or possitive)

###Output
output/submission.tsv


##Programming Language
C++

##Libraries
The most important included library is Boost.

##Installation
###Windows
Follow installation.txt

###Linux
Submodules init and update for root and boost folders

##Context
FIUBA (Buenos Aires Engineering University) 

Exercise for: 75.06 "Organización de datos" (Data Organization)

Date: 06/2015 

##Competition
Team name: Grupo MAS

Position: 184

Score: 0.94643
