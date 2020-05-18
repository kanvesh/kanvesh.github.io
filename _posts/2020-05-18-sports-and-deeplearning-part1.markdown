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
