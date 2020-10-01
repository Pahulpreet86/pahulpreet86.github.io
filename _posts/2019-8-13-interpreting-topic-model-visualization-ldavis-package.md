---
layout: post
title:  "Interpreting Topic Model Visualization - LDAvis Package"
author: Pahul Preet Singh Kohli
categories: [ Topic Modeling, Latent Dirichlet Allocation, LDA, LDAvis, LDA Model Interpretation, NLP, Natural Language Processing] 
image: assets/images/pyldavis.png
description: "Topic Modelling is used to extract topics from a collection of documents.The topics are fundamentally a cluster of similar words. This help in the understanding of hidden semantic structure between words of a large number of the extensive texts at an aggregate level."
comments: false
---

Topic Modelling is used to extract topics from a collection of documents.The topics are fundamentally a cluster of similar words. This help in the understanding of hidden semantic structure between words of a large number of the extensive texts at an aggregate level.


**Inferring the LDA Model visually**:

**Topic Bubble**:
-   The representation includes topics distribution in the 2-dimensional space (left side panel).These topics are represented in the form of bubbles.

-   The larger the bubble, the more frequent is the topic in the documents.

-   A topic model with a low number of topics will have big non-overlapping bubbles, scattered throughout the chart whereas, the topic model with a high number of topics, will have many overlapping small size bubbles, clustered in the chart.

-   Distance between the topics is an approximation of semantic relationship between the topics.
    
-   The topic which shares common words will be overlapping (closer in distance) in comparison to the non-overlapping topic.
    

**Horizontal Bar Graph**:

-   The bar graph shows the frequency distribution of the words in the documents (color: blue).
    
-   The red shaded area describes the frequency of each word given a topic.
    
-   On selecting a topic (clicking on a topic bubble), top 10 words (with the red-shaded area) are shown.
    
-   Hovering over the specific words (in the right panel), only the topic containing the words are visible. The size of the bubble in this scenario describes the weight age of the word on that topic. Higher the weight of the selected word, larger will be the size of the bubble.
    
-   ***Re - Rank words in topics based on their frequency***: by varying λ lambda parameter.
    
	
	Decreasing the lambda parameter, increase the weight of the ratio of the frequency of word given the topic / Overall frequency of the word in the documents.Important words for the given topic moves upward.

  

### References

1.  [https://github.com/bmabey/pyLDAvis](https://github.com/bmabey/pyLDAvis)
    
2.  [https://www.youtube.com/watch?v=IksL96ls4o0](https://www.youtube.com/watch?v=IksL96ls4o0)

