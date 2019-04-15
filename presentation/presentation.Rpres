Natural Language Processing: Next word Prediction
========================================================
author: James Francisco PhD
date: April 14, 2019
autosize: false
width: 1920
height: 1080

### COURSERA - Data Science Specialization Capstone.

### APP LINKS:

* [Next Word Prediction Shiny App](https://jrfanalytics.shinyapps.io/NLP_Capstone/)
* [GitHub url](https://github.com/JamesFrancisco/JHU-Capstone)

1. Introduction
========================================================

Natural Language Processing or
[NLP](https://en.wikipedia.org/wiki/Natural_language_processing)
is a field of computer science with the interaction between computers and human
languages.
One on the oldest NLP problem related to computer word prediction is
[Claude Shannon's](https://en.wikipedia.org/wiki/Claude_Shannon)
problem of assigning a probability to a word, _Shannon_ used
[n-grams](https://en.wikipedia.org/wiki/N-gram),
defined as a contiguous sequence of `n` items, from a given sequence of text or
speech, to compute probabilities of English sentences.

The Markov assumption states that the probability of a word depends only on
the most recent $n-1$ tokens, thus `n-grams` can be used to predict next word
probability. 

***

In a given text or corpus the conditional probability of seen a word $w_n$ using
_Maximum Likelihood Estimation_ (MLE) is:

$$P(w_n | w_1...w_{n-1}) = \frac{c(w_1...w_n)}{c(w_1...w_{n-1})}$$

There are several smoothing algorithms that uses precomputed probabilities
and back-off weights, the _Stupid Backoff_ method is suitable for web applications
and does not calculate normalized probabilities but relative frequencies.

2. Text Preprocess and n-grams
========================================================
### 2.1 DATA:

The dataset for this word prediction app was gathered from three English language sources:

* Blogs
* News
* Twitter

The original english corpus combined over 580 MB of language information. Which summed up to over half a billion characters. After processing the data the model consists of **millions of ngram tokens**.

Data was preprocessed and tokenized with the *quanteda* library.

***

### 2.2 N-GRAMS

All `n-grams` tables have four columns: 
- `sentence`
- `prediction`
- `frequency` (from corpus statistics)
- `probability` (from mle model)

### 2.3 DICTIONARY

`N-gram` tables are parsed with dictionary [cracklib-small](https://github.com/cracklib/cracklib/blob/master/src/dicts/cracklib-small). Words not in the dictionary are sustituted by `UNK`. This step compacts `n-gram` tables and improve app
speed. All `n-gram` tables with `UNK` in predicted column are deleted.


3. Algorithm
========================================================

The predicted word is found by using a simplified version of the
[Stupid Backoff algorithm](https://lagunita.stanford.edu/c4x/Engineering/CS-224N/asset/slp4.pdf),
where probabilities are not calculated, but the more frequent `n-gram` of higher
order found, is used for prediction.

If no `n-gram` is found, the prediction function
returns the most probable unigram: `the`.

***

For additional prediction accuracy were also used:
- Good-Turing Smoothing
- MLE
- linear-regression
- linguistic tweaks


4. How it works and planned future work
========================================================

## How it works

- Enter  your sentence without the final word to be predicted,
inside `Text Area` that can be found in the `Prediction` tab.
Copy and paste is allowed. The entered sentence is parsed and cleaned and the
predicted word is automatically displayed.

- Press one of `Prediction` buttons to append a predicted word to the text area to do further
predictions.

- Press `Clear` to clear the text area.

***

## Future work

Test the code with other languages distict than English. 

Dictionaries of russian, german and finnish are needed, and available, the code does have a functional approach
that should work with these other corpus.


