# Unit 12 - Tales from the Crypto

------------------

## **Objective:**

Use natural language processing to understand the sentiment in the latest news articles featuring Bitcoin and Ethereum.

## **1. Sentiment Analysis**

1. All of the required libraries were imported.

2. A newsapi client was created.

3. Using the 'get.everything' function for newsapi, Bitcoin and Ethereum news articles were fetched.

4. Sentiment scores for Bitcoin and Ethereum were created using the polarity_scores function of the SentimentIntensityAnalyzer tool from Vader.  The scores were organized into a dataframe:

Bitcoin Sentiment Scores:

![](images/1-btc-sentiment.png)

Ethereum Sentiment Scores:

![](images/2-eth-sentiment.png)

5. The sentiment for Bitcoin and Ethereum were then described:

Bitcoin Sentiment Description:

![](images/3-btc-describe.png)

Ethereum Sentiment Description:

![](images/4-eth-describe.png)

### **Conclusion**

Bitcoin had the highest mean positive score of 0.14.

Ether had the highest compound score of 0.836.  

Ether had the highest positive score of 0.212.

## **2. Natural Language Processing**

### **Tokenizer**

1. The required libraries and tools were imported.

2. Lemmatizer was instantiated and a list of stopwords was created.

3. A tokenizer function was created that removed puncuation, created a tokenized list of words, lemmatized words into root words, converted words to lowercase, and removed the stop words.  The tokenizer function was applied to the Bitcoin and Ethereum dataframe text columns.  A new column was added to the two dataframes containing these tokens:

Bitcoin Dataframe (tokens):

![](images/5-btc-dataframe-tokens.png)

Ethereum Dataframe (tokens):

![](images/6-eth-dataframe-tokens.png)

### **NGrams and Frequency Analysis**

1. Bigrams were generated for Bitcoin and Ethereum using the ngrams tool.

BTC Bigrams:

![](images/7-btc-bigrams.png)

ETH Bigrams:

![](images/8-eth-bigrams.png)

2. The pre-defined 'token_count' function was used to get the top 10 words for Bitcoin and Ethereum.

BTC Top 10 Words:

![](images/9-btc-top10.png)

ETH Top 10 Words:

![](images/10-eth-top10.png)

### **Word Clouds**

1. Necessary libraries and tools were imported.

2. The 'WordCloud' tool was appled to the processed Bitcoin and Ethereum dataframe text.

Bitcoin Word Cloud:

![](images/11-btc-wordcloud.png)

Ethereum Word Cloud:

![](images/12-eth-wordcloud.png)

## **3. Named Entity Recognition**

1. Spacy was imported and loaded.

2. The concatenated strings of all the Bitcoin text and the Ethereum text was used to run the NER processor.  Visualizations of both were produced.

Bitcoin NER Visualization:

![](images/13-btc-ner.png)

Ethereum NER Visualization:

![](images/14-eth-ner.png)

The entities were then listed for Bitcoin and Ethereum

Bitcoin Entities:

![](images/15-btc-entities.png)

Ethereum Entities:

![](images/16-eth-entities.png)