---
layout: project
title: Computer Vision Algorithms 
date: February, 2016
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/Lena_edge.bmp?raw=true
keywords: Keywords - Computer Vision, C++, Image Processing Algorithms
---

# Overview

As part of a computer vision course that I took during my masters the weekly homeworks were about understanding image processing algorithms and writing the code to implement them without using any preexisting computer vision libraries. 

# Software 

I chose to write my software in C++ which can all be found <a href="https://github.com/MikhailTodes/computer_vision_functions" target="_blank">here</a>.

The functions implemented were: 

* Identifying Connected Regions
* Morphological Operations
* Histogram Equalization and Lighting Correction
* Colour Segmentation
* Canny Edge Detector
* Hough Transform

# Image Results of Tested Algorithms

<figure align="middle">
     <img class="one" style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/CV_results/region_detection.png?raw=true">
     <figcaption>Identifying connected regions and colouring each segment differently.</figcaption>
</figure>

<figure align="middle">
     <img style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/CV_results/morph_ops.png?raw=true">
     <figcaption>Using morphological operations to remove noise and fill in broken regions.</figcaption>
</figure>

<figure align="middle">
     <img style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/CV_results/histo_light.png?raw=true">
     <figcaption>Histogram equalization and lighting correction.</figcaption>
</figure>

<figure align="middle">
     <img style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/CV_results/skin_detect.png?raw=true">
     <figcaption>Colour segmentation by training with an image of only skin.</figcaption>
</figure>

<figure align="middle">
     <img style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/CV_results/canny_edge.png?raw=true">
     <figcaption>Canny Edge Detection</figcaption>
</figure>

<figure align="middle">
     <img style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/CV_results/hough_lines.png?raw=true">
     <figcaption>Using the hough Transform to find lines that fit the edges.</figcaption>
</figure>