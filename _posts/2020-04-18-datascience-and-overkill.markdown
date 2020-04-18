---
layout: post
title:  "Data Science and Overkill"
date:   2020-04-18 20:11:51 -0400
categories: [data science, analytics]
---


`TL;DR Data Scientists do not come cheap. Use them wisely.`


Building machine learning models requires considerable amount of time, effort and skill. That much is well known. But what maybe not be obvious is that improving the performance of these models over and above a baseline is an exercise with greatly diminishing returns. Data science leaders would do well to understand the cost of iteratively fine-tuning these models and gauge it against business impact.

<!--more-->
`Don't use an sledgehammer to crack a nut`


Lets say you are trying to classify survey comments as positive, neutral or negative. It is pretty easy to come up with a rudimentary keyword-based model that gets to, lets say, 70% accuracy. And this could be done in a single day. However, to improve this baseline model by more than 10%-15%, you might have run it through the whole gamut - natural language processing, feature engineering, complex modeling, the works. This exercise is obviously resource intensive and might take several weeks to complete. So who should decide how sophisticated the model should be? Use case.


`One size does not fit all...`


If you are modeling where exactly a tropical cyclone is going to have its landfall, errors can be extremely costly. However if you are power company who just wants to know how many days it is likely to snow in December, it does not matter if you are not accurate on a day-by-day basis as long as you are near the mark in aggregate. In the earlier case, it is imperative that we understand all possible nuances and spend great amounts of energy in making sure that the model is as accurate as possible. In the latter case, just looking up the average number of snow days over the last 5 years may be good enough for the use case and a model may not be required at all.


<img src='/assets/dilbert-jargon.jpeg'>


There is a lot of hype and expectation around data science and it is easy to get lost in the buzz of it all. Data science is undoubtedly a game changer, but it is essential for data scientists to focus on business impact, for that is what we will be judged on, in the long run.

<i> This blogpost was first published as a LinkedIn article in Dec 2016 </i>
