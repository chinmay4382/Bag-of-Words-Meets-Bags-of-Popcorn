# Kaggle: Bag of Words Meets Bags of Popcorn


*Information extracted from the [Kaggle corresponding page](https://www.kaggle.com/c/word2vec-nlp-tutorial/data)*.

### Data Set

The labeled data set consists of 50,000 IMDB movie reviews, specially selected for sentiment analysis. The sentiment of reviews is binary, meaning the IMDB rating < 5 results in a sentiment score of 0, and rating >=7 have a sentiment score of 1. No individual movie has more than 30 reviews. The 25,000 review labeled training set does not include any of the same movies as the 25,000 review test set. In addition, there are another 50,000 IMDB reviews provided without any rating labels.

### File description

+ __labeledTrainData__ - The labeled training set. The file is tab-delimited and has a header row followed by 25,000 rows containing an id, sentiment, and text for each review.

+ __testData__ - The test set. The tab-delimited file has a header row followed by 25,000 rows containing an id and text for each review. Your task is to predict the sentiment for each one.

+ __unlabeledTrainData__ - An extra training set with no labels. The tab-delimited file has a header row followed by 50,000 rows containing an id and text for each review.

+ __sampleSubmission__ - A comma-delimited sample submission file in the correct format.

### Data fields

+ __id__ - Unique ID of each review
+ __sentiment__ - Sentiment of the review ; 1 for positive reviews and 0 for negative reviews
+ __review__ - Text of the review
