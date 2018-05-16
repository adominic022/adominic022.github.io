---
layout: post
title: Sarcasm Detection
excerpt_separator:  <!--more-->
---

## Sarcasm?

<em>Sarcasm</em> is a linguistic phenomenon in which people state  the opposite of what they actually mean. Common in literature and in spoken words, it is the use of irony to convey one's resentment or to mock. 

While banter is good-humored and more of a playful conversation of sorts, sarcasm is sharp: it is meant to hurt and otherwise mock with irony.

![placeholder](https://blogs.nvidia.com/wp-content/uploads/2018/01/twitter-taggedsarcasm2.png)

# So how does it work?

## It's pretty hard

Sarcasm is definitely on the farther end of difficulty when it comes to human expression. It's difficult for humans to understand, let alone computers. Humans are used to using tone of voice and expression, or emoticons and hashtags on social media to relay their sarcasm to their readers/listeners. 

Another fact that makes it difficult is the use of conversational and situation context, as well as, well, common sense and general knowledge of the world. This of course, makes teaching AI unique human linguistic traits just <em> wonderfull</em>. 

Both problems are a <strong>Classification</strong> problem. When given a piece of text as input, we want to guess if it is of sarcastic quality. 

## Approaches & Methods

### Rule Based
Rule-based approaches attempt to identify sarcasm through specific evidences. These evidences are captured in terms of rules that rely on indicators of sarcasm. They  use  Google  search  in  order  to  determine  how  likely  a simile is. They present a 9-step approach where at each step/rule, a simile is validated using the number of search results. A strength of this approach is that they present an
error analysis corresponding to multiple rules.

![placeholder](https://image.slidesharecdn.com/cs626-sarcasmandthwarting-nov13-131115101715-phpapp02/95/sarcasm-thwarting-in-sentiment-analysis-iitbombay-30-638.jpg?cb=1384510712)

 Hashtags are often used by  tweet  authors  to  highlight  sarcasm,  and  hence,  if  the  sentiment  expressed  by  a
hashtag does not agree with rest of the tweet, the tweet is predicted as sarcastic.  

The first uses a parse–based lexicon generation algorithm that creates parse trees of sentences and identifies situation phrases that bear sentiment. If a negative phrase occurs in a positive sentence, it is predicted as sarcastic. 

#### Statistical
A variety of classifiers have been experimented for sarcasm
detection. Most work in sarcasm detection relies on SVM, with sequential minimal optimization and linear regression. Other approaches include using Chi-squared for identifying discriminating features, or Naive-Bayes combined with SVM for labeling features. 

### Machine Learning
similarity between word embeddings as features for sarcasm detection.
They augment features based on similarity of word embeddings related to most con-gruent and incongruent word pairs, and report an improvement in performance. The augmentation is key because they observe that using these features alone does not suffice.

Combinations of convolutional neural network,
LSTM followed by a DNN are the usual approaches taken. They compare their approach against recursive SVM, and show an improvement in case of deep learning architecture.

## History
First paper on sarcasm detection featured in 2006, with study of lexicon indicators becoming popular the following year. 
Discovering sarcastic patterns was an early trend in sarcasm detection. Several approaches dealt with extracting patterns that are indicative of sarcasm, or carry implied sentiment. These patterns may then be used as features for a statistical classifier, or as rules in a rule-based classifier.

![placeholder](https://qph.fs.quoracdn.net/main-qimg-a6aeed99e114164f365212053447cfb7-c)
Using Twitter Hashtags as labels for twitter datasets became popular around 2013, with it being an easy label to use. This can be commonly seen in other papers, but has often problems due to complex type of sarcasm used in tweets.

### Present
A recent trend in sarcasm detection is the use of context. The term context here refers to any information beyond the text to be predicted, and beyond common knowledge. Context may be incorporated in a variety of ways, using it as supplementary data or information from the source to improve results and learning.

# Issues
Sarcasm detection suffors from 3 main problems: data, feature, and classification. Although hashtag-based labeling can provide large-scale supervision, the quality of the dataset may become doubtful. This is particularly true in case of use of #not to indicate insincere sentiment.  
For example, 

> "I totally love bland food. #not"
 

The speaker expresses sarcasm through #not. In most reported works that use hashtag-based supervision, the hashtag is removed in the pre-processing step. This reduces the sentence above to 
’I love bland food’ - which may not have a sarcastic interpretation, unless author’s context is incorporated

One question that many papers deliberate is if sentiment can be used as a feature for sarcasm detection. The motivation behind sarcasm detection is often pointed as sarcastic sentences misleading a sentiment classifier. However, several approaches use sentiment as an input to the sarcasm classifier. It must, however, be noted that these approaches require ‘surface polarity’  the apparent polarity of a sentence

Sarcasm is an infrequent phenomenon of sentiment expression. This skew also reflects in datasets.

# The Future

### Coverage of different forms of sarcasm
 we described four species of sarcasm: propositional, lexical, like-prefixed and illocutionary sarcasm. We observe that current approaches are limited in handling the last two forms of sar-
casm:  like-prefixed  and  illocutionary.  Future  work  may  focus  on  these  forms  of sarcasm.

### Culture-specific aspects of sarcasm detection
sarcasm is closely related to language/culture-specific traits. Future approaches to sarcasm detection in new languages will benefit from understanding such traits, and  incorporating  them  into  their  classification  frameworks. show that American and Indian annotators may have substantial disagreement in their sarcasm annotations - however, this sees a non-significant degradation in the
performance of sarcasm detection
![placeholder](https://sg.malverninternational.com/wp-content/uploads/2017/01/languages.png)

### Deep learning-based architectures
Very few approaches have explored deep learning-based architectures so far. Future work that uses these architecture may show promise.

Sarcasm Detection
https://arxiv.org/pdf/1602.03426.pdf
http://aclweb.org/anthology/D17-1051
https://www.researchgate.net/figure/Architecture-of-our-sarcasm-detection-approach_fig2_280997051
https://qz.com/801813/teaching-ai-how-to-be-sarcastic-is-totally-the-easiest-thing-ever/
https://pdfs.semanticscholar.org/f1a1/949aab6d40372e0a025fe8f135c220ca0ca3.pdf
https://gate.ac.uk/sale/lrec2014/arcomem/sarcasm.pdf
https://arxiv.org/pdf/1607.00976.pdf
