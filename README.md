# 603_classProject
603 Big Data Platforms Class Project that involve a twitter sentiment analysis. The aim was to use data from the social media platform, Twitter, to track the spread of tweets (via like and retweet metrics) which contain positive sentiment as compared to those that contain negative sentiment. Sentiment Analysis, also called opinion mining, is a popular subset of the broader field of NLP; it is related to analyzing the divergence of documents.


### Code Description 
The code implementation for this project covers the Big Data diagram. The implementation of this project would be divided into two main parts  (file). 
First, we have the file “gettingTwitterFeeds” which is the file where we create the host app with the socket connected to the Spark streaming services. For Spark streaming, we used the library Tweepy, which will help us with the authentication and manage the feeds data that we get from Twitter. The authentication process would need access and consumer keys from the Twitter API that are provided with the developer account. The file “gettingTwitterFeeds” provide a function calls “MyStreamListener” which filters out the number of tweets and saves the data for the necessary transformations. Another function on this file is “send_tweets,” this function is authenticated to the Twitter servers and helps out to filter tweets by language or specific hashtags with the option track. 

The second file for the implementation of this code is “Twitter_SentimentAnalysis.” This file is like the “driver” file of our sentiment analysis implementation, where we create our analysis algorithm. This file is where we start the Spark streaming instances. This file process all the data from the Twitter feeds and creates a Dataframe. We are considering data as the creation of the tweet, text, and source of the tweet. Then, we are implementing some transformations and cleaning of the data for the implementation of our sentiment analysis. After that, our sentiment analysis would be base on VADER-Sentiment-Analysis. VADER (Valence Aware Dictionary and Sentiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments depressed in social media. After getting all the results from the sentiment analysis, we will store all the results and data in MongoDB. After that, MongoDB would be the platform to retrieve the data for our final sentiment analysis. 

### Implementation Instructions
For the Implementation of the code we recommend to have the following libraries: 
- pip install pymongo
- pip install findspark
- pip install pyspark
- pip install vaderSentiment
- pip install ipython
- pip install pandas
- pip install tweepy
- pip install sockets
- pip install jsonlib
- pip install strings
- pip install regex
- pip install --user -U nltk
- pip install pymongo
- pip install os-sys
- pip install requests

**Steps to execute the code** 
- First, we will need to fill out the variable that holds the keys for the Twitter API access. The variables are in the file “gettingTwitterFeeds.” There are two types of keys, which are public and secrete for access and consumer token.  Add the access token key to the variable “access_token,” the secret access key would be in the variable “access_secret.” After that, we need to put the consumer key in the variable “consumer_key,” and the secret consumer key would be saved in the variable “consumer_secret.”

- We can then select the output file in the variable “OUTPUT_FILE” and control the number of tweets in the variable “TWEETS_TO_CAPTURE.”

- Next, we can run all the all cell that is in the file “gettingTwitterFeeds.” ( since it is a Jupyter Notebook) 

- Then, we move to the next file, “Twitter_SentimentAnalysis.” For this file, we just need to run all the cells available in this notebook. Note, we recommend doing a small stop after we reach the cell that contains the command “ssc.start()”  because here is where we start the streaming, and we can go to the file “gettingTwitterFeeds” to see when we reach the desired number of tweets. 

- After that, we finish executing all the reminder cells for the Jupyter notebook file Twitter_SentimentAnalysis.
