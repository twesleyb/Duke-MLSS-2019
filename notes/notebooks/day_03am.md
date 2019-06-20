# An introduction to natural language processing.
__Lecture by Lawrence Carin__
Duke University Electrical and Computer Engineering

Although NLP has not yet reached the level of human performance, it is rapidly
approaching this benchmark.

Goal: the automated processing and understanding of language.
Analysis and synthesis of text to make decision.

## Applications
Problem: It would take a long time for a human to analyze written reports of a 
product. ML can do this.
Sentiment analysis.
Translation of human language. 
Automatic synthesis of text.
Summary and synthesis of text.
Automatic caption of images.

## How can ML analyze text?
ML is good at classification problems. 
This is a classification problem. 
Binary classification can be solved by logistic regression.

Challenge: converting text to numerical values. The training set it text.
Approach: a dictionary of words and their index. Count the frequency of words
in a bit of text. This is the bag of words model. Order does not matter.
This approach is problematic when order matters! e.g. "not bad" versus "bad".

## A new model: Word embeddings.
Map every word to a vector, embeddings. aka word vector.
Map every word to a position in space. A geography of words.
Semanitcally similar words are close in space.
The ML algorithm will learn where in 2D space that word lives.

Can a word with multiple meanings reside in multiple places?
Machine learning is decades old. Of course if you were to read the New York
Times, you may be lead to believe that ML was invented last year!
Google has done this for every word that exists!

Will the machine learn the implicit sterotypes and meanings embedded into
words by history/societies????
Yes, it would! The machine will reflect our own biases!

## Word to vector (word2vec)
A dictionary fo looking up a words "definition" its m-dimensional vector.
How do we learn these word vectors?
m is typically 300. Why 300? Because it works!! 
We are playing catch up trying to understand how these algorithms work!

## How does this work?
Take a sentence:
```
<bos> This is an example of text <eos>

```
Map these words to their vector. If they are related, then they are close in
space.

|---|---|
| This | ... |
| [2,1,...,m]|

Given the nth word, predict the n+1 word.

Word2vec -> h -> output Y-v (v words in vocabulary)
softmax

## Continuous bag of words model (CBOW).


---------------
#### Aside

What is science?
evaluating relationships between ideas and forming hypotheses.
evaluating relationships between experimental observations and forming conclusions.

If you were to start trying to learn a foreign language today, it would be hard!
So learning programming

Google is amassing all this data.

Dooms day view.
Data can be monetized. Money is power. Divide between those with power and
those without growing rapidly. 

Automated hypotheis generation [science](https://f1000.com/work/item/6997588/resources/6345363/pdf)
Improving the pace and quality of research with scientific computing.
* Perform research faster
* Synthesis of academic publications
* Hypothesis generation
* Reproducibility

Humans are error prone and slow!

---------------
