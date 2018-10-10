# Kaggle: Bag of Words Meets Bags of Popcorn


  ### classifier :
  ### Multi Layer Perceptron
 - The multi layer perceptron consists of ```1 input layer, 3 hidden layer,and 1 output layer```
 - The first 4 layer consists ```RELU``` function as activation function and at the output layer ```SIGMOID``` function as activation layer
 - Each layer is followed by Batch Normalization and Dropout layer
 - The loss function considered is  ```binary_crossentropy```
 - The optimizer used is ```Adam optimizer```
 - The metrics used to evaluate is ```Accuracy```
  
+  feature extraction technique :
  
     + With Word2Vec vector representation of words (see [Kaggle tutorial](https://www.kaggle.com/c/word2vec-nlp-tutorial/details/part-3-more-fun-with-word-vectors)) (__300__ features)
 
 ## Results : Prediction accuracy scores
 
 ### MLP

 + Using Word2Vec: Score= 0.8709
 
  
