---
layout: post
title:  "Introduction to Named Entity Recognition (NER)"
author: Pahul Preet Singh Kohli
categories: [ SpaCy, Stanford NER, NER, Named Entity Recognition, NLP, Natural Language Processing] 
image: assets/images/ner.jpeg
description: "Named Entity Recognition is extraction of named entities and their classification into predefined categories such as location, organization, name of a person, etc."
comments: false
---


**Named Entity Recognition**: is extraction of named entities and their classification into predefined categories such as location, organization, name of a person, etc.
The named entity is any real words object denoted with a proper name.
This helps to recognize entities in the document, which are more informative and explains the context.



***Example***: Michael Jordan of the Chicago Bulls is getting a 10-hour Netflix documentary in 2019

##### *Named Entities*:
Name: Michael Jordan
Group: Chicago Bulls

  

## **Approaches for NER**:

  

1.  **Hand Based NER Rules**: is based on extracting named entity using human-made set rules. These rules are based on the pattern in grammar, syntactic or orthographic feature of the text.
    
	
	  

	***Example***: Michael Jordan of the Chicago Bulls is getting a 10-hour Netflix documentary in 2019

	  

	***POS Tags***:

	('Michael', 'NNP'), ('Jordan', 'NNP'), ('of', 'IN'), ('the', 'DT'), ('Chicago', 'NNP'), ('Bulls', 'NNP'), ('is', 'VBZ'), ('getting', 'VBG'), ('a', 'DT'), ('10-hour', 'JJ'), ('Netflix', 'NNP'), ('documentary', 'NN'), ('in', 'IN'), ('2019', 'CD')

  

	***Hand Based Rule***: NNP (Proper Noun) and starts with capital letter

	***Named Entities Extracted through Hand Based  Rule***: Michael, Jordan, Chicago, Bulls, Netflix

  
  
  
  
  
  

2.  **Machine Learning Based NER System**: converts named entity recognition into a classification problem. 

	This requires annotated training dataset to create the feature vector for each word for the model to learn. 

	Many different classifiers have been used to perform machine-learned based NER, with conditional random fields (CRF) preferred choice.
    

  

4.  **Using Pre-trained Model**: which are available online and are trained on a large corpus text.
    
	
	1.  **SpaCy**: is a trained model on OntoNotes 5 corpus.
	    	
		***Example***: Michael Jordan of the Chicago Bulls is getting a 10-hour Netflix documentary in 2019

		  

		***Spacy Output***: ('Michael Jordan', 'PERSON'), ('the Chicago Bulls', 'ORG'), ('Netflix', 'PERSON'), ('2019', 'DATE')

	  

	2.  **Stanford NER**: is a Java implementation of a Named Entity Recognizer.  
The software provides a general implementation of (arbitrary order) linear chain Conditional Random Field (CRF) sequence models.
	
	    ***Example***: Michael Jordan of the Chicago Bulls is getting a 10-hour Netflix documentary in 2019
	    

		 
		***Stanford NER Output***:

		Type: PERSON, Value: Michael
		Type: PERSON, Value: Jordan
		Type: ORGANIZATION, Value: Chicago
		Type: ORGANIZATION, Value: Bulls
		Type: ORGANIZATION, Value: Netflix
		Type: DATE, Value: 2019

	  
	  
	  
	  

**Reference**:

1.  [https://towardsdatascience.com/named-entity-recognition-applications-and-use-cases-acdbf57d595e](https://towardsdatascience.com/named-entity-recognition-applications-and-use-cases-acdbf57d595e)
    
2.  [https://www.kdnuggets.com/2018/08/named-entity-recognition-practitioners-guide-nlp-4.html](https://www.kdnuggets.com/2018/08/named-entity-recognition-practitioners-guide-nlp-4.html)
    
3.  [https://www.codementor.io/bofinbabu/introduction-to-named-entity-recognition-ner-k584v86r6](https://www.codementor.io/bofinbabu/introduction-to-named-entity-recognition-ner-k584v86r6)
    
4.  [https://towardsdatascience.com/named-entity-recognition-applications-and-use-cases-acdbf57d595e](https://towardsdatascience.com/named-entity-recognition-applications-and-use-cases-acdbf57d595e)
    
5.  [https://prateekvjoshi.com/2013/02/23/what-are-conditional-random-fields/](https://prateekvjoshi.com/2013/02/23/what-are-conditional-random-fields/)
    
6.  [https://medium.com/ml2vec/overview-of-conditional-random-fields-68a2a20fa541](https://medium.com/ml2vec/overview-of-conditional-random-fields-68a2a20fa541)
    
7.  [https://medium.com/explore-artificial-intelligence/introduction-to-named-entity-recognition-eda8c97c2db1](https://medium.com/explore-artificial-intelligence/introduction-to-named-entity-recognition-eda8c97c2db1)
    
8.  [https://towardsdatascience.com/named-entity-recognition-with-nltk-and-spacy-8c4a7d88e7da](https://towardsdatascience.com/named-entity-recognition-with-nltk-and-spacy-8c4a7d88e7da)

