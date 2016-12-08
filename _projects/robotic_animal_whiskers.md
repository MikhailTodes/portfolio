---
layout: project
title: Robotic Animal Whiskers
date: August, 2016
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/robot_rat.jpg?raw=true
keywords: Keywords - Analog/Digital signal processing, PCB design, Micro-Soldering, Programming
permalink: "robotic_animal_whiskers"
---
# Overview

For my final project during my masters degree I worked in Professor Mitra Hartmann's lab. I was part of the team developing a robotic whisker system that is based on everything learnt in the Neuroscience side of the lab.

# Video
The video below shows a single whisker connected up. The signals being produced in response to my hand brushing the whisker in different directions are mapped and plotted to a 2 dimensional plane. The slow response seen in the video has to do with the speed of plotting and not the response of the whisker itself.

<div class="container"  align="middle">
     <iframe width="560" height="315" src="https://www.youtube.com/embed/YWnmRgqLRSM" frameborder="0" allowfullscreen></iframe>
</div>

# Follicle

A rat whisker is made up of nothing but hair, and so all the sensing is done with mechanoreceptors in the follicle. The robotic whiskers follow this design. A small strain gauge is placed on the top and bottom of each protruding end of an Aluminium cross. This forms the follicle and the whisker is connected to the centre of the cross. An example of a follicle can be seen in the images below:

<div class="container"  align="middle">
    <img class="one" style='text-align: center; height: 22%; width: 22%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/whisker/f1.jpg?raw=true">
    <img class="two" style='text-align: center; height: 22%; width: 22%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/whisker/f2.jpg?raw=true">
</div>

As the whisker is brushed, the cross will deform in response. Forces and moments can be determined based on this deformation measured by each of the strain gauges. 

The follicles will be attached to the inside of the morphologically accurate model of a rats head and whisker array as seen in the images below:

<div class="container"  align="middle">
    <img class="one" style='text-align: center; height: 22%; width: 22%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/whisker/rat1.jpg?raw=true">
    <img class="two" style='text-align: center; height: 22%; width: 22%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/whisker/rat2.jpg?raw=true">
</div>

This model was made by taking 3D scans of a rats head and using <a href="http://nxr.northwestern.edu/digital-rat" target="_blank">The Digital Rat</a> software (developed in the Hartmann Group) to create a CAD model. From there it was enlarged (7X) and 3D printed.

# Electronics

The PCB (printed circuit board) was designed to read the analog signals coming from the strain gauges. Each board has an ADC (Analog to Digital Converter) that can sample 8 channels (ie. enough for two whiskers with 4 channels each). 

<div class="container"  align="middle">
    <img class="one" style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/whisker/board.jpg?raw=true">
</div>

The chosen ADC and the design of the PCB allow for a bunch of boards to be daisy-chained together and therefore a lot more than 2 whiskers can be used at a given time. The boards can be driven by any microcontroller. When testing this system, a PIC32MX795F512H was used and it was on an <a href="http://hades.mech.northwestern.edu/index.php/NU32" target="_blank">NU32</a> development board designed at Northwestern University.

# Software

### C
The C code was written to program the PIC32  microcontroller. There are two different modes that the system can be run in:

* Stream Mode
* Dump Mode

In the stream mode, the PIC32 serially receives samples from the ADC for the user requested number of channels. This is then sent to the MATLAB side of things for a streaming plot. In the dump mode, the the requested number of channels are sampled and stored for a period specified by the user. When the period has elapsed, the stored data is sent across to MATLAB for the users analysis. 

### MATLAB
The MATLAB code gives the user an interface to specify the mode that the system will be run in as well as the number of channels they will be using. It also shows a plot of the incoming signals during the streaming mode. An example of a plot can be seen in the image below where 8 channels (2 whiskers) are being sampled and streamed:


<div class="container"  align="middle">
    <img class="one" style='text-align: center; height: 60%; width: 60%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/whisker/8out.png?raw=true">
</div>

# Future Work
* Building a custom dedicated microcontroller board to drive the system.
* Speeding up the communication between the ADC, the microcontroller, and MATLAB.
* Building a water proof casing to house the system for seal whisker experiments.