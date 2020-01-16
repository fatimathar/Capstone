#  1.0 Twitter Likes to US President Trump’s tweets using Regression and Classification with NLP

# Project Intro/Objective
Twitter is an important social medium for sharing thoughts. President trump tweets are an important source for to know what is he thinking, doing or thinking of doing.
They are also a source of conflict and controversry. His tweets trigger news article discussions and make headlines. 
He following is at 55M on twitter which keeps his popularity among his supporters and opponents. As he runs for the President of US 2020, popularity on twitter can aid his election popularity and can increase the chances of being elected as President.


# 1.1 Methods used
- EDA
- Machine Learning
- Data Visualization
- Predictive Modeling

# 1.2 Technologies
- Python
-- NLP

# 1.3 Project Description
Given his tweets, I will be doing an analysis on how often does he tweets, 
how he tweets and will try to formulate a response based on his tweets. 
I will also be attempting to predict likes based on the words and sentiment attached to his tweets.

## 1.3.1 Assumptions

Tweets have only been taken into account from the day he was elected as the president
The distribution of the likes from the tweets will fulfill the assumptions of Linear Regression ** Linear relationship ** Multivariate normality ** No or little multicollinearity ** No auto-correlation ** Homoscedasticity
I have done an initial EDA on his tweets. 

## 1.3.2 EDA Findings

Trump tweets show a trend of increase of number of times he is tweeting per day. Which is at the rate of 6 times in 2017, 9 times in 2018 and around 12 times in 2019, which rate is double the number of tweets he was doing in one day back in 2017, his first presidency year.
He is more frequently tweeting between 10:00 am till 10:00. His tweets are coming the rest of the time as well, but not as much as the peak time tweets.
The total number of like that he has racked from the day he was elected as a president till Aug 2019 is, 732,947,115. (read: seven thirty two million, if we accumulate the likes before the time he became president, it will be over 1 billion)
The total number of retweets for the same time period are 171,431,537, more than four times less than the number of likes for the same period.
The Target Variable, favourite_count(number of likes for tweets) is highly negatively skewed (right tailed).
The mean likes per tweet is 88,522.
The top tweeted tweet of his presidency is actually not even a word based tweet. 
It is a video.

## 1.3.3 Data Cleaning
The project required significant amount of cleaning, from removing links, 
other use names,special characters,other language tweets etc. 
RegEx was very useful for cleaning tasks.

## 1.3.4 Modelling - Predicting Likes

I used two bag of word models, i.e. Tfidf, CountVectorizer and TfidfVectorizer.  Best results were obtained using Tfidf. I created a pipeline to perform NLP techniques, Standardisation and Regression with Regularization.I Following ten words were most commonly used in his tweets that got most of the likes.

rocky, fat, merry, country, morning, threaten united, total exoneration, cool.

For predicting the likes, i have used, regression, which gave me score of r-square -3.16. The mean for the prediction was 89,799.
I got improved score with regularization, i.e. 0.12. Also, i used stemming with nltk, which marginally improved the score to 0.135. I also performed Sentiment Analysis on his tweets, 
which did not give any significant findings with how the likes were linked with his positive or negative tweets. Apparently, the longer his tweets were, the more sentiment(positive or negative) they will have. 
Shorter tweets were more of announcement or neutral tweets.

I also performed Classification on the tweets with higher and lower number of likes.Predicting likes was more effective using classification than Regression and it resulted in a 70% accuracy above the baseline. 
I also used Sentiment Analysis to apply classification. My best model was Logistic Regression which gave score around 65%. I used Neural Networks, Decision Trees and Ada Boosting.
Applying Regression to predict the number of likes was one of the challenges faced because the target variable had a skewed distribution. Key findings from the project include that Trump’s positive tweets were classified as having larger number of likes than his negative tweets.
