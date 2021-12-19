# Feature Engineering and Syntactic Similarity

## Bag of Words Model

Bag-of-words models are suitable for a variety of use cases:

* Classification
* Sentiments Detection
* Topic models

Bage of words will create a bias toward the most frequent
words as they have the highest numbers in the document-term matrix. Often these
words do not carry much meaning and could be defined as stop words.

---

## TF-IDF

In our previous example, many sentences started with the words “it was the time of.”
This contributed a lot to their similarity, but in reality, the actual information you get
by the words is minimal. TF-IDF will take care of that by counting the number of
total word occurrences. It will reduce weights of frequent words and at the same time
increase the weights of uncommon words. Apart from the information-theoretical measure,5
 this is also something that you can observe when reading documents: if
you encounter uncommon words, it is likely that the author wants to convey an
important message with them.

