---
layout: post
title:  "Choosing The Right Metrics - A Thought exercise"
date:   2020-05-11 00:11:51 -0400
categories: [analytics, product, metrics, twitter]
---


Hypothetical scenario: I am asked to build a reporting system to monitor the performance of a new recommender system on Twitter. I am told that the A/B test is set up such that half the population get the default sort order and another half get the new algorithmic sort. Here are the metrics I would choose and how I would rank them.
<!--more-->

|Metric|Pros & Cons|
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|---------|
| <b>Daily active Users</b> | **Pro:** Even though the groups start with an equal population,  the successful one might encourage users to log in  more often over time. <br> **Con:** Sharp targeting might be attractive initially  but cause burnout over time (same topics, same people)|
|**Average Time Spent on App**| **Pro:** Great metric to track level of engagement <br> **Con:** Are users spending a lot of time because its taking  a long  time to get to good stuff? |
| **Level of engagement with app  (Likes, retweets)**  | **Pro:** Engagement confirms whether the time spent was really worth it  <br> **Con:** Prolific users tend to dominate engagement metrics. Watch out for the distribution, not just mean values |
| **Level of engagement with community  (follows, sharing to other platforms)** | **Pro:** Increase in such engagement binds a user to the platform  and decreases the likelihood of churn <br> **Con:**  Does not speak for most users who are silent consumers |
