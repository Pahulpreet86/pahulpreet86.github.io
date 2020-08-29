---
layout: post
title:  "Topic Modelling - Latent Dirichlet Allocation"
author: Pahul Preet Singh Kohli
categories: [ Topic Modeling, Latent Dirichlet Allocation, LDA, NLP, Natural Language Processing] 
image: assets/images/topic-modelling.jpeg
description: "Topic Modelling is used to extract topics from a collection of documents.The topics are fundamentally a cluster of similar words. This help in the understanding of hidden semantic structure between words of a large number of the extensive texts at an aggregate level."
comments: false
---

**Topic Modelling**: is used to extract topics from a collection of documents.The topics are fundamentally a cluster of similar words. This help in the understanding of hidden semantic structure between words of a large number of the extensive texts at an aggregate level.

**Latent Dirichlet Allocation**: is a probabilistic modeling technique under topic modeling. The topic emerges during the statistical modeling and therefore referred to as latent.

*LDA tries to map N number of documents to a k number of fixed topics, such that words in each document are explainable by the assigned topics. Each topic has a set of specific words and the weight assigned based on which it describes the probability of the document belonging to that topic.*

**Assumption for LDA**:
1.  Documents exhibit multiple topics
    
2.  A topic is a distribution over a fixed vocabulary
    
**LDA Learning Process**:

1.  Move through the N documents and randomly assign the word to one of the k topics.
    
2.  This gives us the topic distribution over the N documents and vocabulary distribution for each topic, although assignment being random nature is erroneous.
    
3.  Therefore, to improve :
    

	The process moves through each document D, each word w in D, and each topic t in D to calculate:

	1.  p (topic t \| document D): The proportion of words in document D that are currently assigned to topic t.
	    
	2.  p (word w \| topic t): The proportion of assignments to topic t over all documents that come from this word w.
	    

	3.  Then reassign w to a new topic, where we choose a new topic with the highest score for p ( topic t \| document D) * p ( word w \| topic t)
	    
4.  After, a large number of iterations, the modeling reach a steady state where the word assignment to the topic is fairly stable.
	
**LDA Modelling Parameters**:

1.  **Number of Topics k**: the number of topics given to the model to assign words.
    
2.  **Alpha Hyperparameter**: controls the mixture of topics for any given document.
    

	a.  ***Higher Alpha value***: documents will have more mixture of topics
	    
	b.  ***Lower Alpha value***: documents will have less mixture of topics
    

4.  **Beta Hyperparameter**: controls the distribution of words per topic.
    
	
	a.  ***Higher Beta value***: topics will have more words.
	    
	b.  ***Lower Beta value***: topics will have fewer words.
	    

6.  **Number of iterations**: over which the assignments of words to topic become stable.
    

  

**Input Vocabulary**:

The input vocabulary fed to the model can be pruned to restrict modeling of topics over selected words only.

**Pruning Approach**:

1.  **Bag of Words (BOW)**: pruning of vocabulary based on the frequency of words across documents.
    
2.  **TF-IDF**: pruning of vocabulary based on the TF-IDF score of words.
    

  

**Quality of topic modeling**:

**Problem**: there is no ground truth, the model runs unsupervised, so no cross-validation

**Solution**: (relative metric used to compare model performance)

1.  **Perplexity**: hold out a subset of documents, then check their likelihood in the resulting model per word.
    

	-   Perplexity: (exp(-1. * log-likelihood per word))
	    

	-   Lower the perplexity the better model
    

  

2.  **Coherence Score**: is used for assessing the quality of the learned topics.
    

	-   For one topic, the words 𝑖,𝑗 being scored in ∑𝑖<𝑗Score(𝑤𝑖,𝑤𝑗) have the highest probability of occurring for that topic.
	    
	-   Higher the score the better topic quality.
	    
	-   Used to decide the required number of topics in modeling.
	    

*References*:

1.  [https://en.wikipedia.org/wiki/Topic_model](https://en.wikipedia.org/wiki/Topic_model)
    
2.  [https://towardsdatascience.com/light-on-math-machine-learning-intuitive-guide-to-latent-dirichlet-allocation-437c81220158](https://towardsdatascience.com/light-on-math-machine-learning-intuitive-guide-to-latent-dirichlet-allocation-437c81220158)
    
3.  [https://towardsdatascience.com/topic-modeling-and-latent-dirichlet-allocation-in-python-9bf156893c24](https://towardsdatascience.com/topic-modeling-and-latent-dirichlet-allocation-in-python-9bf156893c24)
    
4.  [https://medium.com/@lettier/how-does-lda-work-ill-explain-using-emoji-108abf40fa7d](https://medium.com/@lettier/how-does-lda-work-ill-explain-using-emoji-108abf40fa7d)
    
5.  [http://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf](http://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf)
    
6.  [https://blog.echen.me/2011/08/22/introduction-to-latent-dirichlet-allocation/](https://blog.echen.me/2011/08/22/introduction-to-latent-dirichlet-allocation/)
    
7.  [https://logic.pdmi.ras.ru/~sergey/slides/N14_PhMLtalk.pdf](https://logic.pdmi.ras.ru/~sergey/slides/N14_PhMLtalk.pdf)
    
8.  [https://www.analyticsindiamag.com/beginners-guide-to-latent-dirichlet-allocation/](https://www.analyticsindiamag.com/beginners-guide-to-latent-dirichlet-allocation/)
    
9.  [https://www.cl.cam.ac.uk/teaching/1213/L101/clark_lectures/lect7.pdf](https://www.cl.cam.ac.uk/teaching/1213/L101/clark_lectures/lect7.pdf)
    
10.  [https://www.machinelearningplus.com/nlp/topic-modeling-gensim-python/](https://www.machinelearningplus.com/nlp/topic-modeling-gensim-python/)
    
11.  [http://qpleple.com/perplexity-to-evaluate-topic-models/](http://qpleple.com/perplexity-to-evaluate-topic-models/)

