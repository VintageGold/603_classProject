# 603_classProject
603 Class Project that involve a twitter sentiment analysis

For the code implementation for this project, we created two Jupyter Notebooks : gettingTwitterFeeds and Twitter_SentimentAnalysis.

* The notebook “gettingTwitterFeeds” is responsible for retrieving the Twitter feed from Twitter API and processing using Spark. 

* The notebook “Twitter_SentimentAnalysis” is responsible for ingesting the data from Spark to the Jupyter notebook and for cleaning and processing of the Sentiment Analysis using “vaderSentiment” library. After that, all the results from the analysis are saved into our database in MongodDB.
