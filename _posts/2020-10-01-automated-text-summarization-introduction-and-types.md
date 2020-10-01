---
layout: post
title:  "Automated Text Summarization : Introduction & Types"
author: Pahul Preet Singh Kohli
categories: [Automated Text Summarization, Extractive Summarization, Abstractive Summarization, NLU, Natural Language Understanding] 
image: assets/images/textsummarization.jpeg
description: "Text Summarization is the process of reducing the original text 's size while retaining key information elements and the context."
comments: false
---




Automated Text Summarization is the automated process of reducing the original text 's size while retaining key information elements and the context.

  

The main challenge in automated text summarization is that without a reasonable amount of background knowledge a high reduction rate can not be achieved. 

Anotherchallenge, is we can not be sure that the automated summarizer has not missed any important information from the source.

  

The automated text summarization approaches are categorized in two broad groups:

  

1.  **Knowledge-poor**: depends on solutions which are independent of language and domain.
    

  

2.  **Knowledge-rich**: rely significantly on knowledge base, rules, laws which must be obtained, preserved and are specific for particular language and domain.
    

  

For evaluation of text summarization, a set of metrics called **ROUGE** is calculated.

**ROUGE (Recall Oriented Understudy of Gisting Evaluation)**: is a score based on the similarity in the sequences of words between a human-written text summary and the machine generated summary.

## Types of Auttomated Text Summarization

1.   ### Extractive Summarization (Knowledge-poor)
		-   Extractive summary method draws sentences directly from the text based on a scoring feature.
		    
	
		-   #### Advantages
		    
	
			-   Independent of language and domain.
			    
			-   Easier implementation.
			    
			-   Most important information usually included in extractive summary.
			    
			-   Since the sentences are the same as the source, they can be easily backtracked to understand in depth meaning using the source itself.
			    

		-   #### Disadvantages
		    

			-   Summary generated are synthetic and incoherent.
			    
  

2.   ### Abstractive Summarization (Knowledge-rich)
    

		-   Abstractive summary method generates the summary by interpreting the text using advanced NLU (Natural Language Understanding) techniques.
		    
		-   Includes rephrasing sentences, incorporating information from full text to create summaries alike human-written abstract.
			    

		  
		-   #### Advantages
		    
	
			-    Summary generated are more closer to human created summaries.      
			   


		-   #### Disadvantages
		    
	
			-   Heavily dependent on language and domain.
			    
			-   Summary may not include exactly the same sentences, therefore, will be difficult to backtrack the source sentences for the same.
			    
			-   Most important information might get missed in summary.
			    
			-   Number of sentences in summary depends on the dataset on which it is trained.
  
### References
  
-   [https://www.researchgate.net/publication/2955348_The_Challenges_of_Automatic_Summarization](https://www.researchgate.net/publication/2955348_The_Challenges_of_Automatic_Summarization)
    
-   [https://medium.com/luisfredgs/automatic-text-summarization-with-machine-learning-an-overview-68ded5717a25](https://medium.com/luisfredgs/automatic-text-summarization-with-machine-learning-an-overview-68ded5717a25)
    
-   [http://www.ijcse.com/docs/INDJCSE17-08-04-021.pdf](http://www.ijcse.com/docs/INDJCSE17-08-04-021.pdf)
