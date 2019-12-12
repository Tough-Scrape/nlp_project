# Github NLP Project

## Team: Tough Scrape

#### Jeff Roeder and Sean Oslin

## Goal
Scrape data from GitHub to build a model that can predict the programming language of a repository given the text of the README file.

### Data Source and Methods
- READMEs from starred repositories at GitHub. 
- Initially selected 220 repos. This was winnowed down to 138 based on missing languages, languages we weren't intersted in and empty READMEs.
- Limited to the top 5 languages
- Huge variation in the length of the READMEs, with Python on average the longest, followed by Javascript
- Total number of READMEs for Javascript was greater than the other 4 languages combined
- Extensive text cleaning was done to make the data readable. We intialled failed to leave in the + symbol when we applied REGEX for cleaning. This necessitated rerunning our data
- Filtered out the words with exceptionally high IDF's. We ran this twice.
- The baseline model is the most frequent language in the data. 
- First attempt to model was logistic regression on the entire corpus, only removing the base stopwords and lemmatized words.This model peformed 5% on the train and 1% better on the test
- Second attempt to model used a random forest on the same corpus. This model peformed 6% on the train and 1% better on the test


 