---
layout: post
title:  "Sentiment Analysis - Methods and Pre-Trained Models Review"
author: Pahul Preet Singh Kohli
categories: [ Sentiment Analysis, Text Blob, VADER, Flair, NLP, Natural Language Processing, Python] 
image: assets/images/sentiment.jpeg
description: "Sentiment Analysisis the process of identifying and categorizing opinions expressed in a piece of text to determine whether the attitude of the writer towards a specific subject, product, etc. is positive, negative or neutral."
comments: false
---


## Sentiment Analysis
It is the process of identifying and categorizing opinions expressed in a piece of text to determine whether the attitude of the writer towards a specific subject, product, etc. is positive, negative or neutral.

## Rules - Based Sentiment Analysis
    

-   In this, a series of guidelines/rules are used to evaluate the sentiment expressed towards a particular entity (noun or pronoun) based on its nearness to known positive and negative words (adjectives and adverbs).
    

  

-   Following are the libraries that calculates sentiment score using Rules - Based method:
    

### 1.   Text Blob
	    

-   It provides a simple API for diving into common natural language processing (NLP) tasks such as part-of-speech tagging, noun phrase extraction, sentiment analysis, classification, translation, and more.
	    
	
		  

#### Algorithm / Method for Sentiment Analysis:
1.  TextBlob goes along finding words and phrases it can assign polarity and subjectivity to, and it averages them all together for longer text.
		    		  

2.  A dictionary of words (adjectives) and polarity scores (positive/negative) is created from the lexicon ([en-sentiment.xml](https://github.com/sloria/TextBlob/blob/dev/textblob/en/en-sentiment.xml), an XML document). The value for each word is a dictionary of part-of-speech tags. The value for each word POS-tag is a tuple with values for polarity (-1.0-1.0), subjectivity (0.0-1.0) and intensity (0.5-2.0).
    

  

3.  The Lexicon XML is based on [WordNet3 lexical database](https://wordnet.princeton.edu/) of the English language containing about 150,000 words organized in over 115,000 synsets for a total of 207,000 word-sense pairs.
		    
#### Code:
		
	from textblob import TextBlob
	text="Avengers: Infinity War is a giant battle for which directors Anthony and Joe Russo have given us touches of JRR Tolkien’s Return of the King and JK Rowling’s Harry Potter and the Deathly Hallows. The film delivers the sugar-rush of spectacle and some very amusing one-liners."
	blob = TextBlob(text)
	print(blob.sentiment)

	Output:
	Sentiment(polarity=0.39, subjectivity=1.0)

### 2.   VADER (Valence Aware Dictionary and sEntiment Reasoner)
    



-   It is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media.




-   VADER works best when analysis is done at the sentence level (but it can work on single words or entire novels)




#### Algorithm / Method for Sentiment Analysis:
    

1.  The compound score is computed by summing the valence scores of each word in the [lexicon](https://github.com/cjhutto/vaderSentiment/blob/master/vaderSentiment/vader_lexicon.txt), adjusted according to the rules, and then normalized to be between -1 (most extreme negative) and +1 (most extreme positive).
    

  

2.  The pos, neu, and neg scores from VADER are ratios for proportions of text that fall in each category (so these should all add up to be 1... or close to it with float operation).
    

  

3.  The VADER lexicon is an empirically validated by multiple independent human judges, VADER incorporates a "gold-standard" sentiment lexicon that is especially attuned to microblog-like contexts.
    

#### Code:
	from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer 
	text="Avengers: Infinity War is a giant battle for which directors Anthony and Joe Russo have given us touches of JRR Tolkien’s Return of the King and JK Rowling’s Harry Potter and the Deathly Hallows. The film delivers the sugar-rush of spectacle and some very amusing one-liners."
	sid_obj = SentimentIntensityAnalyzer() 
	sentiment_dict = sid_obj.polarity_scores(text)     
	print(sentiment_dict)

	Output:
	{'neg': 0.123, 'neu': 0.773, 'pos': 0.104, 'compound': -0.2439}



## Machine Learning Based Sentiment Analysis
    

-   The primary role of machine learning in sentiment analysis is to improve and automate the low-level text analytics functions that sentiment analysis relies on.
    

  

-   Following are libraries that use pre-trained ML model for calculation/prediction of sentiment score:
    

  
	
### 1.   Flair
	    

-   Flair’s sentiment classifier is based on a character-level LSTM neural network which takes sequences of letters and words into account when predicting.
    

  

-   Advantages is that it can predict a sentiment for out-of-vocabulary (OOV) words that it has never seen before too.
    

  

-   The Flair sentiment analysis model is trained on IMDB [(Maas et al., 2011)](https://ai.stanford.edu/~amaas/data/sentiment/) dataset for binary sentiment classification containing 25,000 highly polarized movie reviews for training, and 25,000 for testing.
    

#### Code:
	import flair
	from flair.models import TextClassifier
	flair_sentiment = TextClassifier.load('en-sentiment')
	text="Avengers: Infinity War is a giant battle for which directors Anthony and Joe Russo have given us touches of JRR Tolkien’s Return of the King and JK Rowling’s Harry Potter and the Deathly Hallows. The film delivers the sugar-rush of spectacle and some very amusing one-liners."
	sentence=flair.data.Sentence(text)
	flair_sentiment.predict(sentence)
	total_sentiment = sentence.labels
	print(total_sentiment)

	Output:
	[POSITIVE (0.9994151592254639)]
			

### References

-   [https://www.lexalytics.com/technology/sentiment-analysis#rules](https://www.lexalytics.com/technology/sentiment-analysis#rules)
    
-   [https://textblob.readthedocs.io/en/dev/](https://textblob.readthedocs.io/en/dev/)
    
-   [https://planspace.org/20150607-textblob_sentiment/](https://planspace.org/20150607-textblob_sentiment/)
    
-   [https://github.com/cjhutto/vaderSentiment](https://github.com/cjhutto/vaderSentiment)
    
-   [https://medium.com/@b.terryjack/nlp-pre-trained-sentiment-analysis-1eb52a9d742c](https://medium.com/@b.terryjack/nlp-pre-trained-sentiment-analysis-1eb52a9d742c)
    
-   [https://www.aclweb.org/anthology/N19-4010.pdf](https://www.aclweb.org/anthology/N19-4010.pdf)
