---
layout: post
title:  "Name Entity Recognition (NER) - Methods and Pre-Trained Models Review"
author: Pahul Preet Singh Kohli
categories: [ NLTK, Stanford NER, spaCy, Flair, Deep Pavlov, Polyglot NER, NER, Named Entity Recognition, NLP, Natural Language Processing] 
image: assets/images/ner-pretrained.jpeg
description: "NER is extraction of named entities and their classification into predefined categories such as location, organization, name of a person, etc. The named entity is any real words object denoted with a proper name. This helps to recognize entities in the document, which are more informative and explains the context."
comments: false
---



### **Name Entity Recognition**
NER is extraction of named entities and their classification into predefined categories such as location, organization, name of a person, etc. The named entity is any real words object denoted with a proper name. This helps to recognize entities in the document, which are more informative and explains the context.

Following are the pre-trained models used for NER:

- **NLTK**
    - **Algorithm**: The text is tokenized > the tokens are passed through a Part Of Speech (POS) tagger > a parser chunks the tokens based on their POS tags to find named entities.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>NLTK NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">NLTK(nltk.ne_chunk())</td>
    <td class="tg-0lax">ACE 2004</td>
    <td class="tg-0lax">newswire, broadcast news, telephone conversations</td>
    <td class="tg-0lax">MaxEnt classifier</td>
    <td class="tg-0lax">Organization, Person, Location, Date, Time, Money, Percent, Facility, GPE</td>
  </tr>
</table>
<br />
	

- **Stanford NER**
    - Stanford NER is also known as CRFClassifier.
	- **Algorithm**: A CRF is a conditional sequence model which represents the probability of a hidden state sequence given some observations.
	- This is especially useful in modeling time-series data where the temporal dependency can manifest itself in various different forms.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>Stanford NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">3 class</td>
    <td class="tg-0lax">CoNLL 2003 eng, MUC 6, MUC 7, ACE 2002</td>
    <td class="tg-0lax">newswire, broadcast news, telephone conversations</td>
    <td class="tg-0lax">CRFClassifier</td>
    <td class="tg-0lax">Location, Person, Organization</td>
  </tr>
  <tr>
    <td class="tg-0lax">4 class</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">CRFClassifier</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
  </tr>
  <tr>
    <td class="tg-0lax">7 class</td>
    <td class="tg-0lax">MUC 6 and MUC 7(~318 news articles in MUC 6)</td>
    <td class="tg-0lax">newswire</td>
    <td class="tg-0lax">CRFClassifier</td>
    <td class="tg-0lax">Location, Person, Organization, Money, Percent, Date, Time</td>
  </tr>
</table>
<br />
- **spaCy**
    - spaCy is an open-source software library for advanced Natural Language Processing, written in the programming languages Python and Cython.
	- **Algorithm**: Convolutional layers with residual connections, layer normalization and maxout non-linearity. And a novel bloom embedding strategy with subword features is used to support huge vocabularies in tiny tables.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>spaCy NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">en_core_web_sm</td>
    <td class="tg-0lax">OntoNotes(~1745k articles)</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">English multi-task CNN. Assigns context-specific token vectors, POS tags, dependency parse and named entities.</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
  </tr>
  <tr>
    <td class="tg-0lax">en_core_web_md</td>
    <td class="tg-0lax">OntoNotes(~1745k articles)(Vectors - 685k keys, 20k unique vectors (300 dimensions)</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">English multi-task CNN trained on OntoNotes, with GloVe vectors trained on Common Crawl. Assigns word vectors, context-specific token vectors, POS tags, dependency parse and named entities.</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
  </tr>
  <tr>
    <td class="tg-0lax">en_core_web_lg</td>
    <td class="tg-0lax">OntoNotes(~1745k articles)(Vectors - 685k keys, 685k unique vectors (300 dimensions)</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">English multi-task CNN trained on OntoNotes, with GloVe vectors trained on Common Crawl. Assigns word vectors, context-specific token vectors, POS tags, dependency parse and named entities.</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
  </tr>
</table>
 <br />
- **GATE (General Architecture for Text Engineering)**
	- ANNIE (A Nearly-New Information Extraction System) is **rules-based system** that work on different layers of abstraction along the NLP pipeline
	- **Algorithm**: ANNIE comprise of a set of modules comprising a tokenizer, a gazetteer, a sentence splitter, a part of speech tagger, a named entities transducer and a coreference tagger.
	- ANNIE can be used as-is to provide basic information extraction functionality, or provide a starting point for more specific tasks.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>GATE NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">ANNIE</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax">-</td>
    <td class="tg-0lax">Rule-Based(Finite State Machine)</td>
    <td class="tg-0lax">People,Location,Organization</td>
  </tr>
</table>
<br />
- **Flair**
    - Flair is an openly available framework for a range of NLP tasks across different languages.
	- **Algorithm**: A sentence is input as a character sequence into a pre-trained bidirectional character language model. From this LM, we retrieve for each word a contextual embedding by extracting the first and last character cell states.
	- This word embedding is then passed into a vanilla BiLSTM-CRF sequence labeler.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>Flair NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">ner</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">Contextual String Embeddings + BiLSTM-CRF</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
  </tr>
  <tr>
    <td class="tg-0lax">ner-ontonotes</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">Contextual String Embeddings + BiLSTM-CRF</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
  </tr>
</table>
<br />
- **Deep Pavlov**
    - There are two main types of models available: standard RNN based and BERT based.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>Deep Pavlov NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">ner_ontonotes</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">Bi-LSTM+CRF</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
  </tr>
  <tr>
    <td class="tg-0lax">ner_ontonotes_bert</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">BERT+Bi-LSTM+CRF</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
  </tr>
  <tr>
    <td class="tg-0lax">ner_conll2003</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">Bi-LSTM+CRF</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
  </tr>
  <tr>
    <td class="tg-0lax">ner_conll2003_bert</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">BERT+Bi-LSTM+CRF</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
  </tr>
</table>
<br />
- **AllenNLP**
    - fine grained ner: BiLSTM-CRF+ELMo

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>AllenNLP NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">fine grained ner</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">BiLSTM-CRF+ELMo</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
  </tr>
</table>
<br />
- **Polyglot NER**
	- It uses huge unlabelled datasets (like Wikipedia) with automatically inferred entity labels (via features such as hyperlinks).
	- The internal links embedded in Wikipedia articles are used to detect named entity mentions. When a link points to an article identified by Freebase as an entity article,the anchor text is taken as a positive training example.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>Polyglot NER Model</b></th>
    <th class="tg-0pky"><b>Data(vocabulary)</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">Polyglot NER</td>
    <td class="tg-0lax">mostfrequent 100K words and the word</td>
    <td class="tg-0lax">Wikipedia Articles and Freebase</td>
    <td class="tg-0lax">Classifier (feedforward neural network)</td>
    <td class="tg-0lax">Person, Locations, Organizations</td>
  </tr>
</table>
<br />
### **Overview: NER Model Performance**

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky"><b>NER Model</b></th>
    <th class="tg-0pky"><b>Data</b></th>
    <th class="tg-0pky"><b>Data Source</b></th>
    <th class="tg-0pky"><b>Model Description</b></th>
    <th class="tg-0pky"><b>Entities</b></th>
    <th class="tg-0lax"><b>Performance F1 score(Dataset)</b></th>
  </tr>
  <tr>
    <td class="tg-0lax">NLTK</td>
    <td class="tg-0lax">ACE 2004</td>
    <td class="tg-0lax">newswire, broadcast news, telephone conversations</td>
    <td class="tg-0lax">MaxEnt classifier</td>
    <td class="tg-0lax">Organization, Person, Location, Date, Time, Money, Percent, Facility, GPE</td>
    <td class="tg-0lax">0.89 ± 0.11(CoNLL-2003)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Stanford NER Model</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">CRFClassifier</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
    <td class="tg-0lax">87.94%(CoNLL-2003)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Polyglot NER</td>
    <td class="tg-0lax">mostfrequent 100K words and the word</td>
    <td class="tg-0lax">Wikipedia Articles and Freebase</td>
    <td class="tg-0lax">Classifier (feedforward neural network)</td>
    <td class="tg-0lax">Person, Locations, Organizations</td>
    <td class="tg-0lax">71.3%(CoNLL-2003)</td>
  </tr>
  <tr>
    <td class="tg-0lax">spaCyen_core_web_lg</td>
    <td class="tg-0lax">OntoNotes(~1745k articles)(Vectors - 685k keys, 685k unique vectors (300 dimensions)</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">English multi-task CNN trained on OntoNotes, with GloVe vectors trained on Common Crawl. Assigns word vectors, context-specific token vectors, POS tags, dependency parse and named entities.</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
    <td class="tg-0lax">85.85%(OntoNotes 5)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Flairner-fast</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">Contextual String Embeddings + BiLSTM-CRF</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
    <td class="tg-0lax">93.09±0.12%(CoNLL-2003)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Flairner-ontonotes-fast</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">Contextual String Embeddings + BiLSTM-CRF</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
    <td class="tg-0lax">89.7%(OntoNotes 5)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Deep PavlovNer_ontonotes</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">Bi-LSTM+CRF</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
    <td class="tg-0lax">86.4%(OntoNotes 5)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Deep PavlovNer_ontonotes_bert</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">BERT+Bi-LSTM+CRF</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
    <td class="tg-0lax">88.6%(OntoNotes 5)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Deep Pavlovner_conll2003</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">Bi-LSTM+CRF</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
    <td class="tg-0lax">89.9%(CoNLL-2003)</td>
  </tr>
  <tr>
    <td class="tg-0lax">Deep PavlovNer_conll2003_bert</td>
    <td class="tg-0lax">CoNLL 2003 eng(1,393 English news articles)</td>
    <td class="tg-0lax">news articles</td>
    <td class="tg-0lax">BERT+Bi-LSTM+CRF</td>
    <td class="tg-0lax">Location, Person, Organization, Misc</td>
    <td class="tg-0lax">91.7%(CoNLL-2003)</td>
  </tr>
  <tr>
    <td class="tg-0lax">AllenNLP NER Model</td>
    <td class="tg-0lax">OntoNotes(~1745k articles</td>
    <td class="tg-0lax">telephone conversations, newswire, newsgroups, broadcast news, broadcast conversation, weblogs</td>
    <td class="tg-0lax">BiLSTM-CRF+ELMo</td>
    <td class="tg-0lax">Person, Norp, Fac, Org, Gpe, Loc, Product, Event, Work_Of_Art, Law, Language, Date, Time, Percent, Money, Quantity, Ordinal, Cardinal</td>
    <td class="tg-0lax">88.7%(OntoNotes 5)</td>
  </tr>
</table>
<br />
### References

- **NLTK**
    - [https://www.nltk.org/book/ch07.html](https://www.nltk.org/book/ch07.html)
    - [https://mattshomepage.com/articles/2016/May/23/nltk_nec/](https://mattshomepage.com/articles/2016/May/23/nltk_nec/)
   
- **Stanford NER**
    - [https://nlp.stanford.edu/software/jenny-ner-2007.pdf](https://nlp.stanford.edu/software/jenny-ner-2007.pdf)
    - [https://towardsdatascience.com/conditional-random-fields-explained-e5b8256da776](https://towardsdatascience.com/conditional-random-fields-explained-e5b8256da776)
    - [https://prateekvjoshi.com/2013/02/23/what-are-conditional-random-fields/](https://prateekvjoshi.com/2013/02/23/what-are-conditional-random-fields/)
    - [https://nlp.stanford.edu/software/CRF-NER.shtml](https://nlp.stanford.edu/software/CRF-NER.shtml)
    - [https://nlp.stanford.edu/~manning/papers/gibbscrf3.pdf](https://nlp.stanford.edu/~manning/papers/gibbscrf3.pdf)
- **spaCy**
    - [https://spacy.io/models/en](https://spacy.io/models/en)
    - [https://explosion.ai/blog/how-spacy-works](https://explosion.ai/blog/how-spacy-works)
    - [https://spacy.io/models#architecture](https://spacy.io/models#architecture)
- **GATE**
    - [https://gate.ac.uk/overview.html](https://gate.ac.uk/overview.html)
    - [https://www.slideshare.net/dianamaynard/text-analysis-in-gate](https://www.slideshare.net/dianamaynard/text-analysis-in-gate)
    - [https://gate.ac.uk/sale/acl02/acl-main.pdf](https://gate.ac.uk/sale/acl02/acl-main.pdf)
- **Flair**
    - [https://research.zalando.com/welcome/mission/research-projects/flair-nlp/](https://research.zalando.com/welcome/mission/research-projects/flair-nlp/)
    - [http://alanakbik.github.io/papers/coling2018.pdf](http://alanakbik.github.io/papers/coling2018.pdf)
    - [https://github.com/flairNLP/flair](https://github.com/flairNLP/flair)
    - [https://github.com/flairNLP/flair/blob/master/resources/docs/TUTORIAL_2_TAGGING.md](https://github.com/flairNLP/flair/blob/master/resources/docs/TUTORIAL_2_TAGGING.md)
- **Deep Pavlov**
    - [http://docs.deeppavlov.ai/en/master/features/models/ner.html](http://docs.deeppavlov.ai/en/master/features/models/ner.html)
    - [https://towardsdatascience.com/bert-to-the-rescue-17671379687f](https://towardsdatascience.com/bert-to-the-rescue-17671379687f)
    - [http://docs.deeppavlov.ai/en/master/features/overview.html#ner-model-docs](http://docs.deeppavlov.ai/en/master/features/overview.html#ner-model-docs)
    - [http://docs.deeppavlov.ai/en/master/features/models/bert.html](http://docs.deeppavlov.ai/en/master/features/models/bert.html)
- **Allennlp**
    - [http://api.semanticscholar.org/arXiv:1802.05365](http://api.semanticscholar.org/arXiv:1802.05365)
- **Polyglot-NER**
    - [https://arxiv.org/pdf/1410.3791.pdf](https://arxiv.org/pdf/1410.3791.pdf)
    - [https://polyglot.readthedocs.io/en/latest/NamedEntityRecognition.html](https://polyglot.readthedocs.io/en/latest/NamedEntityRecognition.html)
- **Overview: NER Model Performance**
    - [https://drops.dagstuhl.de/opus/volltexte/2016/6008/pdf/OASIcs-SLATE-2016-3.pdf](https://drops.dagstuhl.de/opus/volltexte/2016/6008/pdf/OASIcs-SLATE-2016-3.pdf)
    - [https://nlp.stanford.edu/projects/project-ner.shtml](https://nlp.stanford.edu/projects/project-ner.shtml)
    - [https://spacy.io/usage/facts-figures](https://spacy.io/usage/facts-figures)
    - [https://arxiv.org/pdf/1410.3791.pdf](https://arxiv.org/pdf/1410.3791.pdf)
    - [http://docs.deeppavlov.ai/en/master/features/models/ner.html](http://docs.deeppavlov.ai/en/master/features/models/ner.html)
    - [https://www.arxiv-vanity.com/papers/1904.10503/](https://www.arxiv-vanity.com/papers/1904.10503/)
- [https://medium.com/@b.terryjack/nlp-pretrained-named-entity-recognition-7caa5cd28d7b](https://medium.com/@b.terryjack/nlp-pretrained-named-entity-recognition-7caa5cd28d7b)
- [https://towardsdatascience.com/named-entity-recognition-ner-meeting-industrys-requirement-by-applying-state-of-the-art-deep-698d2b3b4ede](https://towardsdatascience.com/named-entity-recognition-ner-meeting-industrys-requirement-by-applying-state-of-the-art-deep-698d2b3b4ede)

### Dataset
- **NLTK**
    - ACE 2004**:** [https://catalog.ldc.upenn.edu/LDC2005T09](https://catalog.ldc.upenn.edu/LDC2005T09)
    
- **Stanford NER**
    - MUC 6: [https://catalog.ldc.upenn.edu/LDC2003T13](https://catalog.ldc.upenn.edu/LDC2003T13)
    - MUC 7: [https://catalog.ldc.upenn.edu/LDC2001T02](https://catalog.ldc.upenn.edu/LDC2001T02)
    - MUC 6 and MUC 7 : [https://www-nlpir.nist.gov/related_projects/muc/muc_data/muc_data_index.html](https://www-nlpir.nist.gov/related_projects/muc/muc_data/muc_data_index.html)
    - CoNLL 2003: [https://www.clips.uantwerpen.be/conll2003/ner/](https://www.clips.uantwerpen.be/conll2003/ner/)
- **spaCy**
    - OntoNotes Release 5.0: [https://catalog.ldc.upenn.edu/LDC2013T19](https://catalog.ldc.upenn.edu/LDC2013T19)
    - OntoNotes Release 5.0: [https://catalog.ldc.upenn.edu/docs/LDC2013T19/OntoN otes-Release-5.0.pdf](https://catalog.ldc.upenn.edu/docs/LDC2013T19/OntoNotes-Release-5.0.pdf)
- **Flair**
    - CoNLL 2003: https://www.clips.uantwerpen.be/conll2003/ner/
    - OntoNotes Release 5.0: [https://catalog.ldc.upenn.edu/LDC2013T19](https://catalog.ldc.upenn.edu/LDC2013T19)
- **Deep Pavlov**
    - CoNLL 2003: [https://www.clips.uantwerpen.be/conll2003/ner/](https://www.clips.uantwerpen.be/conll2003/ner/)
    - OntoNotes Release 5.0: [https://catalog.ldc.upenn.edu/LDC2013T19](https://catalog.ldc.upenn.edu/LDC2013T19)
