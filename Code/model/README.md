# Kaggle: Bag of Words Meets Bags of Popcorn


### Training the W2V Model
To train a Word2Vec model "unlabeledTrain.tsv" is used which contains 50,000 additional reviews with no labels.
The Word2Vec can learn from unlabeled data, these extra 50,000 reviews can now be used.

   #### There are a number of parameter choices that affect the run time and the quality of the final model that is produced.
   
   + **Architecture**: Architecture options are skip-gram (default) or continuous bag of words. We found that skip-gram was very       slightly slower but produced better results.
   
   + **Training algorithm**: Hierarchical softmax (default) or negative sampling. For us, the default worked well.
   
   + **Downsampling of frequent words:** The Google documentation recommends values between .00001 and .001. For us, values closer  0.001 seemed to improve the accuracy of the final model.
   
   + **Word vector dimensionality:** More features result in longer runtimes, and often, but not always, result in better models. Reasonable values can be in the tens to hundreds; we used 300.
   
   + **Context / window size:** How many words of context should the training algorithm take into account? 10 seems to work well for hierarchical softmax (more is better, up to a point).
   
   + **Worker threads:** Number of parallel processes to run. This is computer-specific, but between 4 and 6 should work on most systems.
   
   + **Minimum word count:** This helps limit the size of the vocabulary to meaningful words. Any word that does not occur at least this many times across all documents is ignored. Reasonable values could be between 10 and 100. In this case, since each movie occurs 30 times, we set the minimum word count to 40, to avoid attaching too much importance to individual movie titles. This resulted in an overall vocabulary size of around 15,000 words. Higher values also help limit run time.

### Training the MLP Model

  #### Parametrs
  
  + [Activation function](https://en.wikipedia.org/wiki/Activation_function): The activation function of a node defines the output of that node given an input or set of inputs
  
  + [Layers](https://en.wikipedia.org/wiki/Multilayer_perceptron#Layers):The MLP consists of three or more layers (an input and an output layer with one or more hidden layers) of nonlinearly-activating nodes. Since MLPs are fully connected, each node in one layer connects with a certain weight   to every node in the following layer. 
  
  + [Learning](https://en.wikipedia.org/wiki/Multilayer_perceptron#Learning) :Learning occurs in the perceptron by changing connection weights after each piece of data is processed, based on the amount of error in the output compared to the expected result.
