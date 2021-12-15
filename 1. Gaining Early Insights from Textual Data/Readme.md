# Gaining Early Insights from Textual Data

Understanding the data is more important. Descriptive statistics provide a reliable and robust insights and help to assess data quality and distribution.
When considering texts, frequency analysis of words and phrases is one of the main methods for data exploration.

---

## Exploratory Data Analysis

Exploratory data analysis is the process of systematically examining data on an aggregated level. Typical methods include ```summary statistics``` for numerical features as well as ```frequency counts``` for categorical features. ```Histograms and box plots``` will illustrate the distribution of values, and time-series plots will show their evolution.

* ```Corpus in nlp``` means a dataset consisting of text documents.

* ```Peculiarities``` in the data often become visible when different subsets of the data are examined. ```Violine plot``` or ```Boxplot``` are the best plots to visulaize such difference.

  * ```Violin plots``` are used when you want to observe the distribution of numeric data, and are especially useful when you want to make a comparison of distributions between multiple groups. The peaks, valleys, and tails of each group’s density curve can be compared to see where groups are similar or different

---

## Simple Text Preprocessing Pipline

SOURCE TEXT ==> CASE-FOLDING ==> TOKENIZATION ==> STOPWORD REMOVAL ==> PREPARED TOKENS

* ```Tokenization``` is the process of extracting words from a sequence of characters
* ```Stopwords```, The most frequent words in text are common words such as determiners, auxiliary verbs, pronouns, adverbs, and so on. These words are called stop words. Stop words usually don’t carry much information but hide interesting content because of their high frequencies. Therefore, stop words are often removed before data analysis or model training.

  * WHY REMOVING STOP WORDS CAN BE DANGEROUS:
    Stop word removal is a coarse-grained rule-based method. Be careful with the stop word lists you are using, and make sure that you don’t delete valuable information. Look at this simple example: “I don’t like ice cream.”
    Both NLTK and spaCy have I and don’t (same as do not) in their stop word lists. If you remove those stop words, all that’s left is like ice cream. This kind of preprocessing would heavily distort any kind of sentiment analysis. TF-IDF weighting, as introduced later in this section, automatically underweighs frequently occurring words but keeps those terms in the vocabulary.

---

## N-Grams

* Two types of word sequences: compound and collections
  * A ```compound``` is a combination of two or more words with a specific meaning.
    * example ```self-confident```
  * ```Collocations``` are words that are frequently used together.
    * example ```united nations```

* unigrams : Sequence of len(single word)->1
* bigrams : Sequence of len->2
* trigrams : Sequence of len->3

```The reason to stick to n ≤ 3 is that the number of different n-grams increases exponentially with respect to n, while their frequencies decrease in the same way```

It is advisable to build bigrams without stop words. If we remove the stop words first and then build the bigrams, we generate bigrams that don't exist in the original text.

---

## Plot Distribution

* One way to visualize the five-number summary of a numerical distribution.
  * BOX PLOT

* Skewness
  * Left Skewness
  * Right Skewness
  * <https://www.analyticsvidhya.com/blog/2020/07/what-is-skewness-statistics/>

  Methods to remove the skewness are:
  * Log Transformation
  * Power Transformation
  * Exponential Transformation
