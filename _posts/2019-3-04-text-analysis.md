---
layout: post
title:  "Text Analysis in Python"
author: Pahul Preet Singh Kohli
categories: [Text Analysis, Sentimental Analysis, Analysis of Readability, NLP, Natural Language Processing, NLTK, Python] 
image: assets/images/text-analysis.jpeg
description: "Text Analysis involves a set of techniques and approaches to transorm textual content to a point where it can be represented as data."
comments: false
---

Text Analysis involves a set of techniques and approaches to transorm textual content to a point where it can be represented as data.        
_Following are the commonly used methods for Text Analysis:_     

- **Word Count** : total number of words.
	```python
	def word_count(text):
	    from nltk import word_tokenize
	    number_of_words=len(word_tokenize(text))
	    return number_of_words

	text="The proverb has deep meaning, which is always useful for a successful life. It conveys the idea that we should always think and then act accordingly. Impulsive actions may lead us to embarrassing and odd situations. As we should always think before we speak, in the same way we should think before we act. Life is full of various factors, the factors which can fascinate us for the moment but may lead us to failure or the factors which can repel immediately but may be the stepping stones to success. For example, going to a movie or playing video games may seem an attractive thing for the time being but can, in the course of time not only disturb one’s studies but also injure our eyes. Therefore, we should always restrain our intuitive and impulsive desires and then act according to what our mind says is right. Even the great men like Gandhi. Nehru, John Kennedy have been prey to their passions and emotions due to which the nations suffered. We should learn from their lives and should always act thoughtfully."
	print("Number of words: ", word_count(text))
	
	Output:
	Number of words:  200
	```          
<br>

- **Average Word Length** :
*Average Word Length = Sum of the total number of characters in each word/Total number of words*
	```python
	def average_word_length(text):
	    from nltk import word_tokenize
	    number_words=len(word_tokenize(text))
	    number_of_char=0
	    for word in word_tokenize(text):
	        number_of_char=number_of_char+len(word)
	    avg_word_len=number_of_char/number_words
	    return avg_word_len

	text="The proverb has deep meaning, which is always useful for a successful life. It conveys the idea that we should always think and then act accordingly. Impulsive actions may lead us to embarrassing and odd situations. As we should always think before we speak, in the same way we should think before we act. Life is full of various factors, the factors which can fascinate us for the moment but may lead us to failure or the factors which can repel immediately but may be the stepping stones to success. For example, going to a movie or playing video games may seem an attractive thing for the time being but can, in the course of time not only disturb one’s studies but also injure our eyes. Therefore, we should always restrain our intuitive and impulsive desires and then act according to what our mind says is right. Even the great men like Gandhi. Nehru, John Kennedy have been prey to their passions and emotions due to which the nations suffered. We should learn from their lives and should always act thoughtfully."
	print("Average word length: ",average_word_length(text))

	Output:
	Average word length:  4.2
	```         

<br>
- **Average Number of Words Per Sentence** :
*Average Number of Words Per Sentence = Total number of words / Total number of sentences*
	```python
	def avg_no_words_per_sentence(text):
	    from nltk.tokenize import sent_tokenize, word_tokenize
	    #Number of sentences
	    no_of_sentences=len(sent_tokenize(text))
	    
	    #Number of words
	    no_of_words=len(word_tokenize(text))
	    
	    #Average word per sentence
	    average_word_per_sentence=(no_of_words/no_of_sentences)
	    
	    return average_word_per_sentence

	text="The proverb has deep meaning, which is always useful for a successful life. It conveys the idea that we should always think and then act accordingly. Impulsive actions may lead us to embarrassing and odd situations. As we should always think before we speak, in the same way we should think before we act. Life is full of various factors, the factors which can fascinate us for the moment but may lead us to failure or the factors which can repel immediately but may be the stepping stones to success. For example, going to a movie or playing video games may seem an attractive thing for the time being but can, in the course of time not only disturb one’s studies but also injure our eyes. Therefore, we should always restrain our intuitive and impulsive desires and then act according to what our mind says is right. Even the great men like Gandhi. Nehru, John Kennedy have been prey to their passions and emotions due to which the nations suffered. We should learn from their lives and should always act thoughtfully."
	print("Average Number of Words Per Sentence: ", avg_no_words_per_sentence(text))
	
	Output:
	Average Number of Words Per Sentence:  20.0
	```         
<br>
 -   **Syllable Count Per Word** :  count the number of syllables in each word of the text by counting the vowels present in the word.  
		```python
		def syllable_count_per_word(word):
		    #lower 
		    word=word.lower()
		    #vowels
		    vowels = "aeiouy"
		    number_of_syllables = 0
		    
		    if word[0] in vowels:
		        number_of_syllables=number_of_syllables+1
		    
		    for index in range(1, len(word)):
		        if word[index] in vowels and word[index - 1] not in vowels:
		            number_of_syllables=number_of_syllables+1
		    
		    if word.endswith("e"):
		        number_of_syllables=number_of_syllables-1
		    
		    if number_of_syllables == 0:
		        number_of_syllables=number_of_syllables+1
		        
		    return number_of_syllables
		    
		print("Number of syllables: ",syllable_count_per_word("Maximum"))
		
		Output:
		Number of syllables:  3
		```             
    
<br>

- **Complex Word Count** : are words in the text that contain more than two syllables.
	```python
	def complex_words(text):
	    from nltk.tokenize import word_tokenize
	    words=word_tokenize(text)
	    complex_words=[word for word in words if syllable_count_per_word(word)>2 ]
	    return complex_words

	text="The proverb has deep meaning, which is always useful for a successful life. It conveys the idea that we should always think and then act accordingly. Impulsive actions may lead us to embarrassing and odd situations. As we should always think before we speak, in the same way we should think before we act. Life is full of various factors, the factors which can fascinate us for the moment but may lead us to failure or the factors which can repel immediately but may be the stepping stones to success. For example, going to a movie or playing video games may seem an attractive thing for the time being but can, in the course of time not only disturb one’s studies but also injure our eyes. Therefore, we should always restrain our intuitive and impulsive desires and then act according to what our mind says is right. Even the great men like Gandhi. Nehru, John Kennedy have been prey to their passions and emotions due to which the nations suffered. We should learn from their lives and should always act thoughtfully."
	print("Complex words: ",complex_words_round(text))

	Output:
	Complex words:  ['useful', 'successful', 'accordingly', 'Impulsive', 'embarrassing', 'situations', 'fascinate', 'immediately', 'attractive', 'Therefore', 'intuitive', 'impulsive', 'desires', 'according', 'Kennedy', 'emotions', 'suffered', 'thoughtfully']
	```         
 
 <br>

-   **Sentimental Analysis** : is the process of determining whether a piece of writing is positive, negative or neutral.
 
	-	**Polarity** :  refers to identifying _sentiment orientation_ (positive, neutral, and negative) in written or spoken language.
			 The polarity score is a float within the range [-1.0, 1.0] where +1.0 is very positive and -1.0 is very negative.
			 
	- **Sentiment score categorization** : categorizing text based on their polarity score.           
					**Most Negative**: Polarity Score below -0.5                                 
					**Negative**: Polarity Score between -0.5 and 0          
					**Neutral**: Polarity Score equal to 0          
					**Positive**: Polarity Score between 0 and 0.5       
					**Very Positive**: Polarity Score above 0.5      

			 
	- **Subjectivity** :  in the sentence refres to opinions, allegations, desires, beliefs, suspicions, and speculations.
		The subjectivity is a float within the range [0.0, 1.0] where 0.0 is very objective and 1.0 is very subjective.
		```python
		from textblob import TextBlob

		def sentiment_score_category(polarity_score):
		      if polarity_score < -0.5:
		      return "Most Negative"
		    if (polarity_score >= -0.5 and polarity_score < 0):
		      return "Negative"
		    if polarity_score == 0:
		      return "Neutral"
		    if (polarity_score > 0 and polarity_score <= 0.5):
		      return "Positive"
		    if polarity_score > 0.5:
		      return "Most Positive"

		text = TextBlob("These laptops are horrible but I've seen worse")
		print("Polarity Score: ", text.sentiment.polarity)
		print("Subjective Score: ", text.sentiment.subjectivity)
		print("Sentiment Score Category: ", sentiment_score_category(text.sentiment.polarity))

		Output:
		Polarity Score: -0.7
		Subjective Score: 0.8
		Sentiment Score Category: Most Negative
		```           


<br>
-   **Analysis of Readability** : is calculated using the Gunning Fox index .	
	***Average Sentence Length** =  number of words /  number of sentences*        
	***Percentage of Complex words** = (number of complex words / number of words) * 100*	         
	***Gunning Fog Index** = 0.4 * (Average Sentence Length + Percentage of Complex words)*            


	```python
	def gunning_fog_index(text):
	    #Average_number_word_per_senetence
	    avg_word_per_sentence=avg_no_words_per_sentence(text)
	        
	    #percentage of complex words
	    percentage_complex_words=(len(complex_words(text))/word_count(text))*100
	    
	    #gunning fox index score
	    gunning_fog_score=0.4*(avg_word_per_sentence+percentage_complex_words)
	    
	    return round(gunning_fog_score,2)

	text="A paragraph is a self-contained unit of a discourse in writing dealing with a particular point or idea. A paragraph consists of one or more sentences. Though not required by the syntax of any language, paragraphs are usually an expected part of formal writing, used to organize longer prose."
	print("Gunning Fof Index: ", gunning_fog_index(text))

	Output:
	Gunning Fox Index:  14.61
	```
