---
layout: project
title: Traffic Counter
date: February, 2016
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/traffic_counter.png?raw=true
keywords: Keywords - Computer Vision, C++, Python, Tracking
---

# Overview

As a final project for the computer vision course that I took, I developed software that would count the number of vehicles passing under a bridge on a highway.

# Video

<div class="container"  align="middle">
     <iframe width="560" height="315" src="https://www.youtube.com/embed/kT1PV1s3nKs" frameborder="0" allowfullscreen></iframe>
</div>

# Vehicle Tracking

In order to track the vehicles two different algorithms were tested. The first one was sequential imaging 
and was implemented using C++. The second used background subtraction and was written in Python. They both made use of the OpenCV library.

* Sequential Imaging – This is taking two consecutive frames of a video feed and comparing them to each other. Each time a pixel in the same position on the two frames has a different value it is recorded. Therefore only objects that are moving from frame to frame show up. Other operations are applied to reduce noise and only identify vehicles as apposed to other moving objects.

* Background Subtraction – Here a few frames at the beginning of the video are used to train the algorithm. A calculation is done to as to the probability of a pixel being part of the background. The longer the pixel is static, the higher its probability. Once a decent background image has been determined, a subtraction of this from any other frame would leave just the objects moving in the foreground. Again other operations are applied to reduce noise and only identify vehicles as apposed to other moving objects.