# Project 3: Web Scraping & Classification

### Problem Statement

What characteristics of a post on Reddit are most predictive of the overall interaction on a thread (as measured by number of comments)?


### Executive Summary

Reddit is one of the most popular online communities with millions of members visiting each month.  The social app hosts a number of popular subreddits from politics to gaming, with more and more subreddits popping up each month.  It is a powerful medium that lets users disseminate to a wide audience.  

As you may know, we have been tasked to find out what characteristics are the most predictive at determining what makes a “hot”  reddit post through user engagement.  Engagement can be measured in a couple of ways.  Firstly though the numbers of upvotes a reddit gets, and secondly, through the number of comments on a reddit post.  For the purposes of this analysis, we have chosen to focus on the number of comments.  

So how do we go about figuring out how to define the best predictors? Well, we build models.  In this analysis we looked at three different models: a random forest model, a bagging model, and a logistic regression model.  By tuning three different models, we were able to narrow down the best predictors and the best model to do the job.  Before we started modeling, we sourced our data from Reddit, and cleaned it up.  We used a porter stemmer, and a TfidfVectorizer to to vectorize the reddit data (the titles).  From there, we did a train test split on our data, and ran our models.  We were then able to narrow down key words that had the most predictive power. 



### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|author|object|Reddit|User name of the author of the reddit post| 
|title|object|Reddit|Title of the reddit post|
|created|float64|Reddit|Date reddit was created|
|num_comments|int64|Reddit|Number of comments on the reddit post|
|subreddit|object|Reddit|The subreddit that the reddit post belongs to|
|score|int64|Reddit|The number of upvotes the reddit has|
|upvote_ratio|float64|Reddit|The percentage of upvotes from all votes on the reddit|
|length_time|float64|Calculated|The length of time a reddit post has been up|
|num_words|int64|Calculated|The number of words in the reddit title|
|num_chars|in64|Calculated|The number of characters in the reddit title|


### Conclusion

The models all had varying results in terms of the weight given to words that impacted the modeling.  The logistic regression model favored words such as 'hate', 'pride', 'actually' and 'year'.  The random forest model favored words such as 'upvote_ratio', 'num_chars', 'new', 'pride', and 'dog'.  The bagging model favored words such as 'upvote_ratio', 'new', 'year', 'pride', and '2022'. 'Pride' was common to all three models, while 'year' was common to the bagging and the logistic regression models.  

When selecting words to pass into the model, there were certain words that increased the scores.  Newsworthy words such as 'ukraine' and 'depp' tended to boost the scores.  Topical words such as '2022' and 'pride' also helped increase the scores.  Interestingly enough, 'dog' increased the scores, whilst 'cat' decreased them.  The biggest predictive power by far came from the reddit score, which is the popularity of a reddit post (as measured by number of upvotes).  Words such as 'spoiler' and 'season' also seemed to boost the scores.

In addition, when looking at popular subreddits, political-themed subreddits proved to be very popular (as measured by the numbers of comments).  This aligns with what I found when tuning the model: words that reflected the "news of the day" proved to be effective predictors.  

As far as models go, random forest generally performed better than the other two models (logistic and bagging).  It allowed the most tuning of the r-squared score, continually improving the scores whereas the other models hit a point of diminishing returns. It also had the best training scores of all three models (though it should be noted that it tied with the bagging model for test data scores).  

In terms of metrics, the random forest model had the best overall accuracy score, as well as the best sensitivity and f1-scores.  The logistic regression model, on the other hand, had the best precision and specificity scores. The bagging model performed the worst of the three.  

My recommendation, therefore, is to use the random forest model.  In terms of what characteristics have the most predictive power for overall interaction, as mentioned above, political and newsworthy terms seemed to effective predictors.  Reddits about Ukraine, the school shooting, and the Depp/Heard defamation suit were all good predictors, as well as temporal words like 'time', 'year', '2020', and 'today. Finally, words related to the entertainment medium such as 'spoiler' and 'season' seemed to be good predictors too.
