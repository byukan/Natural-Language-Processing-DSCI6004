# Lab Feedback

## Week1-1: Welcome and NLP Overview
Looks Good
## Week1-2: Text Processing & Regular Expressions I
Looks Good
## Week1-3: Regular Expressions II
SpamLord:

email_pattern = "|".join([email_pattern1, email_pattern2]) Yes!!!!
## Week1-4: Segmenting, Tokenizing, & Stemming
Looks Good
## Week2-1: Text Encoding
Looks Good
## Week2-2: Edit Distance
```python
if s1[i] == s2[j]:
    # there is no need to add a 0
    # substitutions = previous_row[j] + 0  
    substitutions = previous_row[j]
else:
    substitutions = previous_row[j] + cost_sub
```
when you get a chance try the make change problem. Its a good interview question
## Week2-3: Language Modeling I
This is a unigram model because we are only returning one word, not because there are no conditional dependencies


## Week2-4: Language Modeling II
Heaps Law:
Don't print out large variables. This makes it hard to grade and hard to review when you go back.


## Week3-1: Spelling Correction
```python
spell_errors = {}
with open("../../../corpora/spell_errors.txt") as f:ultrarelativistic@gmail.com
    # Look for current word as a value in common spelling error dictionary
    # If found, use that correction.
    # XXX: there dictionary words in the values which introduces new errors ☹
    common_errors = [key for key,values in spell_errors.items()
                                  if word in values]

    # Prefer common errors, then edit distance 0, then 1, then 2; otherwise default to word itself.
    candidates = (common_errors or
                  known(edits0(word)) or
                  known(edits1(word)) or
                  known(edits2(word)) or
                  [word])

    print(candidates)
    return max(candidates, key=counts.get)

```
## Week3-2: Word Tagging
```python
months_pattern = [(r'(%s)$'%month, 'MONTH') for month in months]

#use str.format instead. looks cleaner and works better
months_pattern = [(r'({})$'.format(month), 'MONTH') for month in months]
```
## Week3-3: Named Entity Recognition (NER)
Looks Good
## Week3-4: Review/Project Check In

## Week4-1: Information Retrieval I
```python
docs = set(self.inv_index[query[0]])

#change to for word in query[1:] because doc is already the set of query[0] so the intersection at query[0] will return doc
for word in query:
    docs = docs.intersection(set(self.inv_index[word]))
```
## Week4-2: Information Retrieval II
```python
counts = [Counter(doc) for doc in self.docs]  # list of counter object for each documnet in self.docs

self.tfidf = {}
for word in self.vocab:
    for d in range(len(self.docs)):
        if word not in self.tfidf: #this is always true because you only go through each word once. no need for if statement
            self.tfidf[word] = {}

        tf = counts[d][word]  # term frequency

        if tf != 0:
            df = len(self.inv_index[word]) # document frequency
            self.tfidf[word][d] = (1 + np.log(tf)) * np.log(len(self.docs)/df)
        else:
            self.tfidf[word][d] = 0


#this should be one line
#words_in_query = set(query)
words_in_query = set()
for word in query:
    words_in_query.add(word)

#this is jaccard similarity
for d, doc in enumerate(self.docs):
    words_in_doc = set(doc)
    scores[d] = (len(words_in_query.intersection(words_in_doc))
                 / float(len(words_in_query.union(words_in_doc))))
```
## Week4-3: Information Retrieval Project

## Week4-4: Chatbots I
use list.insert() to add your_are and father to pyschobabble
## Week5-1: Chatbots II
Looks Good
## Week5-2: Naive Bayes
No Solution
## Week6-1: Sentiment Analysis
Looks Good
## Week6-2: Non-negative Matrix Factorization (NMF)
Topic 0 is too general to label is business. The other 3 are very specfic though which suggests that you should try more topics
## Week6-3: Latent Dirichlet Allocation (LDA)
Looks Good
## Week6-4: Topic Modeling Project

## Week7-1: Word2Vec
Looks Good
## Week7-2: Doc2Vec

## Week7-3: Everything2Vec

## Week7-4: Future of NLP Guest Lecture

## Week8: Final Presentation:
