# Natural Language Processing with Reddit

#### Project by: Andrew Picart

### Contents

- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Data](#Data)
- [Conclusion and Recommendations](#Conclusion-and-Recommendations)

## Problem Statement

The classification of parody sites and actual news would be very useful in determining posts that misclassify parody news as real.  Misinformation is very prevalent in our society today and having a model that could potentially alert and prevent the misclassification of posts.

There are two objective in this project.  The first is to web scrape reddit's API. Data was collected from two different subreddits.  The second part of the project involves taking the data from both subreddits and using models to predict which one a new post would be classified as accurately as possible. The models will take Natural Language Processing data to classify the unseen posts.

## Executive Summary

By reddit's own tagline, they are the "front page of the internet." Users can post links and also selftext of pretty much anything. There are almost an infinite amount of subreddits for any niche topic you can think of.

Of the thousands of subreddits and probably millions of posts, the ones focused on in this project are r/news and r/TheOnion. r/TheOnion is a parody news subreddit, with all links coming from theonion.com.  r/news can be any news related from any website.  By comparing these two, a model can be constructed to properly classify and differentiate between the two subreddits.

## Data

Data was collected from [r/news](http://reddit.com/r/news) and [r/TheOnion](http://reddit.com/r/TheOnion) over the course of 4 days using reddit's API.

The .cvs files can be found [here](/Datasets)

## Conclusions and Recommendations

While there are a lot of overlap between the two subreddits, there is enough data to determine the correct subreddit in about 86% of the time (using the nmb model).  The NMB model also had a specificity rate of .89. In the context of this project, we would want to reduce Type I error.  A false positive would be indicative of a someone posting an onion article and thinking it were real. Given that the null model is accurate 58% of the time, the NMB model beats the null model.  The model is perfect in the bias/variance tradeoff in that the train and test data are almost identical.

If given more time, I would try and work increase the specificity rate.  Being able to detect the parody site and not misclassify it as real news would be my main goal.
