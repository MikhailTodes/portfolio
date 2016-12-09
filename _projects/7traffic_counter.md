---
layout: project
title: Traffic Counter
date: February, 2016
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/traffic_counter.png?raw=true
keywords: Keywords - Computer Vision, C++, Python, Tracking
permalink: "traffic_counter"
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

# Counting Algorithm

Counting the vehicles presented the problem of having to uniquely identify vehicles and keep track of them between frames. I decided instead to use my own method that would be a little less computationally intense. I did this by adding the vertical position coordinates of all identified vehicles within a certain band as can be seen in the figure below:

<div class="container"  align="middle">
    <img class="one" style='text-align: center; height: 40%; width: 40%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/count_algo_band.png?raw=true" align="middle">
</div>


The total value inside the band decreases as the vehicles get closer to the 0 (bottom end of the frame). If at any stage there is an increase in the band's collective total (by an amount roughly the size of the band so as to avoid counting small jumps in the vehicles tracking), a vehicle must have entered and the count is incremented. This way the only variable that needs to be tracked between frames is the band's collective total. This band size can then easily be increased or decreased to be tuned for different cameras. 