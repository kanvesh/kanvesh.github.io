---
layout: post
title:  "Can we make Test Cricket more fun?"
date:   2020-05-18 00:11:51 -0400
categories: [sports, product, deep learning, cricket]
---

Americans are amused at this to no end, but the original format of cricket, the Test Match, runs for a full 5 days. These long matches however, are seeing a slow decline over time, and the sport in recent times been dominated by shorter formats, but the 5-day Test still remains the highest echelon for greatness in cricket. I myself like Test Cricket over all other formats, but I have to admit that I simply don't have the patience to watch a game slowly unfold over 5 days. Is there a way to make the viewing experience more fun and crisp? I give it a shot using a simple VGG Image Classifier here.
<!--more-->

**One can build deep learning models with very small datasets**

One of the fast.ai lectures mentioned the story of someone who tried to build an image classifier that distinguishes between cricket and baseball using only _ training images and achieved _ % accuracy. Deep learning was supposed to be about these massive neural networks learning from huge datasets, but this story opened up the possibility of using transfer learning a very small dataset to build something that was fairly accurate.
So I thought if I can use something like this to identify which parts of a cricket video had some action going on, and which parts did not, we can use that to filter out uninteresting portions. Turns out that it is not that difficult after all.

**Some background about cricket**

The unit of play in Cricket is the _Over_ and each over has six _balls_(each ball is like a pitch in baseball). The bowler running in to throw the ball is called the delivery stride. The delivery stride is effectively when the action begins and the action ends in multiple ways depending on how the batsman tacked the ball. Once the action ends, the ball is technically dead and the bowler begins his trudge back to the starting point to begin another delivery stride. Over an entire match's duration, a ball only stays alive less than 25% of time and cutting the match content down to this period has the potential to make Test cricket more watchable.

**Identifying the delivery stride**

While the conditions for what constitutes the _end_ of a ball is harder, given the multiple possibilities, the conditions _start_ of a ball is fairly consistent. It starts with the bowler running from behind the umpire and delivering the ball at crease. To identify the start of a ball, I manually annotated a bunch of images as either 'Delivery Stride' or 'Other'. Here are some images after they have been passed through an edge detector. If you squint your eyes, you will notice that there is a really distinct pattern among the images that are part of delivery stride.

<br/>
![](/assets/greensight-1/edge-images.png)
<br/>

I added a couple of layers to a pre-built VGG neural network and trained it using these annotated images, the results were really good. I tested on video from another match and the results were equally good. The model seems to have generalized well. The model need not to be right on every frame, as long as it would identify a cluster of frames with high likelihood of being the _start_ of the ball. And by simply assuming that the _duration_ of the ball being alive on an average is 6-8 seconds, one can identify passages of play with a great amount of accuracy. Here is an example of an [full over (vimeo link)](https://vimeo.com/419878487){:target="_blank"} that was cut using the method described above. The [processed output](https://vimeo.com/419878633) cuts the video runtime from 3 minutes to 30 seconds, but preserves all the action)
