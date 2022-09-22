# Sentiment Analysis Model in Python

The dataset used is the movie review polarity data described in ['A Sentimental Education: Sentiment Analysis Using Subjectivity Summarization Based on Minimum Cuts'](https://www.aclweb.org/anthology/P04-1035/). The dataset itself is available [here](http://www.cs.cornell.edu/People/pabo/movie-review-data) (section "Sentiment polarity datasets"). It contains 1000 positive and 1000 negative reviews, each tokenised, sentence-split (one sentence per line) and lowercased. The model is evaluated using average 10-fold cross-validation accuracy.

In the [*polarity_predictor.ipynb*](polarity_predictor.ipynb) notebook, we have created a sentiment analysis model to classify movie reviews as either postive or negative. The original baseline system utilised a Bag-of-Words representation. We have designed a Bag-of-Bigrams and Bag-of-Trigrams implementation for the purpose of experimentation. There are various parameters associated with the model, which alter the structure of these features also, inlcuding:

* Clipping counts
* Performing negation
* Removing stop words
* Lemmatising words
* Using additional features

There are more specific details given about these parameters in the notebook itself. In the notebook, we also experiment with various learning models and output the results of these to CSV files which are stored in the *output* folder. The learning models which we experimented with include:

* Multinomial Naive Bayes
* Logistic Regression
* Decision Tree Classifier
* SVM Classifier
* Random Forest Classifier

We experiment with the baseline model with and without the features above, and also conduct a number of additional experiments with different combinations of features.

The *baseline* system which uses Naive Bayes achieved an average 10-fold cross-validation accuracy of 82.9%.  
The best-performing model used a Logistic Regression learning model with default parameters, and achieved an average 10-fold cross-validation accuracy of 86.6%.  

The experiments and changes to code are discussed in the [*polarity_predictor.ipynb*](polarity_predictor.ipynb) notebook.
