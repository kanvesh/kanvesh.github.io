---
layout: post
title:  "Choosing The Right Metrics (A Thought exercise)"
date:   2020-05-11 00:11:51 -0400
categories: [analytics, product, metrics, twitter]
---

Product success has several dimensions and it means different things to different people. It is therefore important to choose the right set of proxy metrics to measure success and really think through how these numbers have the potential to mislead. Here I consider a hypothetical scenario where I am asked to build a reporting system to monitor the performance of a new recommender system on Twitter. This is how I would approach a set of metrics for this use case.
<!--more-->

|**Metric**|**Pros & Cons**|
|----------|----------------|
| <b>Daily active Users</b> | **Pro:** Users logging in more often is a big win <br><br> **Con:** Sharp targeting might be attractive initially  but cause burnout over time (same topics, same people)|
|**Average Time Spent on App**| **Pro:** Great metric to track level of engagement <br><br> **Con:** Are users spending a lot of time because its taking  a long  time to get to good stuff? |
| **Level of engagement with app**  _(likes, retweets)_  | **Pro:** Proactive engagement confirms whether the time spent was really worth it  <br><br> **Con:** Prolific users tend to dominate engagement metrics. Watch out for the distribution, not just mean values. |
| **Level of engagement with community**  _(follows, sharing to other platforms)_ | **Pro:** Increase in such engagement binds the user to the platform and decreases the likelihood of churn <br><br> **Con:**  Does not speak for most users who are silent consumers |
| **Feedback surveys and focus groups** | **Pro:** No traditional metric captures addiction or general wellbeing <br><br>  **Con:** Expensive and has potential for bias|

**Conclusion**: Even though the first two metrics are widely measured and used, the last three metrics are likely to be better predictors of success for a platform like Twitter.

**Notes:**
<i>
1. I have not considered downstream metrics like revenue generated from ads etc., because, for one, it is a second order metric with tenuous links to the feature change and moreover it seems to be [accepted wisdom](https://youtu.be/raIUQP71SBU?t=586) that focusing on product experience is the best way to revenue.
2. A feature that works great for a small set of users and so-so for the rest still can come out looking good on average. Pay attention to distribution.
3. Watch out for novelty effect. Any change is interesting at first, but only if the interest is sustained over time, can the feature claim to be of real impact.
4. Remember that measurement is not an exercise to prove your hunch. It is an opportunity to explore and truly understand the dynamics at play.
</i>

If you have a comment about the blogpost, I would be happy to [hear](mailto:gmail.com) from you!
