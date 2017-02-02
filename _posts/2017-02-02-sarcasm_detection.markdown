---
layout: post
title:  "The Sarcasm Detection Exercise"
date:   2017-Feb-02 10:00:43 +0530
categories: jekyll update
author: "Priya Ananthasankar"
---

So it was election time in the US and I was looking at the tweets thinking, now that is a load of cynicism and sarcasm. I was also taking my Applied NLP course at the same time and voila, we have an idea. How can we detect sarcasm as a sentiment?
It sure is a negative sentiment but people say "Wow" and "Yeah right" about something that is negative? So here is what we did:

1. We collected 3000 tweets with #sarcasm and #sarcastic. 
2. Three of us manually annotated the tweets to see if they were really sarcastic.
3. We calculated the Fleiss Kappa metric for the annotation which told us how much we (as annotators) agree on sarcasm for each tweet.
4. We cleaned the tweets
5. We ran machine learning algorithms like Maximum Entropy, Reverse Polarity, KNN, Naive Bayes, Perceptron, Support Vector Machine.
6. Average Accuracy = 65%, Baseline = 50% - Not bad huh?

Here is the link: https://github.com/priyaananthasankar/sarcasm_detector

Enjoy.
