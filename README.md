# Sentiment_Analysis_Methods___Lexicon_based

Lexicon-based sentiment analysis is a method of sentiment analysis that relies on predefined sentiment lexicons or dictionaries containing words with associated sentiment scores. This approach determines the sentiment of a piece of text by calculating the sentiment scores of the words present in the text and aggregating them to obtain an overall sentiment score. The sentiment score could be a continuous value (ranging from negative to positive) or discrete labels (such as positive, negative, neutral).Lexicon based approach can further be divided into two categories:

1. **Dictionary based approach**: consists of a list of predefined set opinion words collected manually. The primary assumption behind this approach is that synonyms have the same polarity as the base word, while antonyms have opposite polarity.
        
2. **Corpus based approach**: The approach employs semantic and syntactic patterns to ascertain the sentence’s emotion.
   - **Statistical Approach**: The rough idea behind this approach is that if it appears in positive texts more than negative texts, then it is more likely to be positive or vice versa.
   - **Semantic Approach**: In this approach, the similarity score is calculated between tokens that are used for Sentiment Analysis.


### Pros of Lexicon-Based Sentiment Analysis:

- **Simplicity and Speed**: Lexicon-based methods are relatively easy to implement and computationally efficient, making them suitable for quick sentiment analysis tasks.
- **Interpretability**: The method provides insights into which words contribute to the sentiment score, making it easy to understand the reasons behind the sentiment classification.
- **No Training Data Required**: Lexicon-based methods don't require labeled training data, as they rely on predefined lexicons.
- **Domain Adaptation**: Lexicons can be specialized for specific domains or languages, allowing sentiment analysis in niche areas.

### Cons of Lexicon-Based Sentiment Analysis:

- **Limited Vocabulary**: The performance heavily relies on the quality and coverage of the lexicon. Uncommon or domain-specific words might not be present in the lexicon, leading to inaccurate results.
- **Context Ignorance**: Lexicon-based methods don't consider the context in which words are used, potentially leading to incorrect sentiment assignments.
- **Neutral Words**: The sentiment of neutral words may be inaccurately classified if the lexicon does not adequately capture their nuances.
- **Lack of Nuance**: Lexicon-based methods might not capture subtle variations in sentiment, such as sarcasm or mixed emotions.
- **Difficulty Handling New Words**: Lexicon-based methods struggle with new or slang words that are not present in the lexicon.
- **They are prone to human bias**. For instance, if the people preparing the dictionary don’t have sufficient domain knowledge, the method won’t yield accurate results.

  
## Type of sentiment analysis model with score:
- [AFINN](https://github.com/fnielsen/afinn) : is a pre-built sentiment lexicon that assigns scores to words based on their sentiment. The sum of scores for all words in a text determines the overall sentiment score.

 - [SentiWordNet](https://github.com/harika-bonthu/Lexicon-based-SentimentAnalysis): is a lexical resource that provides sentiment scores for words based on their synsets in WordNet.

 - [VADER](https://github.com/cjhutto/vaderSentiment) (Valence Aware Dictionary and sEntiment Reasoner): is a rule-based sentiment analysis tool specifically designed for social media text. It uses predefined rules and a sentiment lexicon to analyze sentiment in the text.

 - [TextBlob](https://textblob.readthedocs.io/en/dev/quickstart.html): is a Python library for processing textual data. It provides a consistent API for diving into common natural language processing (NLP) tasks such as part-of-speech tagging, noun phrase extraction, sentiment analysis, and more. TextBlob uses a simple Naive Bayes classifier and a built-in sentiment lexicon to determine sentiment.


## How to use
In this repository, we return the polarity and score obtained using these methods for an arbitrary csv file in the form of a new dataframe.

### Example
<pre>
Sentiment_Analysis_lex('path of csv file','text column on dataset',list of methods)
</pre>

If you set 'all' for list of methods, all of methods run for your dataset.
<pre>
Sentiment_Analysis_lex('path of csv file','text column on dataset','all')
</pre>

else you can select some methode in a list for example:
<pre>
Sentiment_Analysis_lex('path of csv file','text column on dataset',['AFINN','TextBlob'])
</pre>


### Resources:
1. https://link.springer.com/article/10.1007/s10462-022-10144-1
2. https://github.com/fnielsen/afinn
3. https://github.com/harika-bonthu/Lexicon-based-SentimentAnalysis
4. https://github.com/cjhutto/vaderSentiment
5. https://textblob.readthedocs.io/en/dev/quickstart.html
6. https://github.com/MHDBST/PerSenT/blob/main/dev.csv

