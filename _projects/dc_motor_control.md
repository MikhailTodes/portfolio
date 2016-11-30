---
layout: project
title: DC Motor Control
date: March, 2016
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/dc_motor_circ.jpg?raw=true
keywords: Keywords - PID Control, DC Motor, Digital/Analog Electronics, Communication Protocols
---

# Overview

The aim of this project was to build an intelligent motor driver. The system can follow an input reference position/trajectory, velocity, or torque to spin a brushed DC motor's shaft with an inertial load attached. The system has feedback control implemented with a digital PID controller in the software and an encoder attached to the motor. The system also has current sensed feedback. Inputs are received with a user interface written in MATLAB. This software also allows for output plotting as visual and quantitative feedback for the user.

# Video

<div class="container"  align="middle">
     <iframe width="560" height="315" src="https://www.youtube.com/embed/LpN0bZk4wZE" frameborder="0" allowfullscreen></iframe>
</div>

# Hardware

* Brushed DC Motor with a plastic bar attached to the shaft as an inertial load.
* Encoder chip.
* A breakout board for the DRV8835 H-Bridge.
* A battery pack to supply the motor.
* A breakout board for the MAX9918 current-sense amplifier (Attached to ADC on the PIC32).
* PIC32 Microcontroller with an <a href="http://hades.mech.northwestern.edu/index.php/NU32" target="_blank">NU32</a> breakout board.
* An <a href="http://www.nscope.org/" target="_blank">NScope</a> digital oscilloscope and an LCD screen were used for feedback when testing.

The ciruit was connected up as shown in the diagram bellow:
<div class="container"  align="middle">
    <img class="one" style='text-align: center; height: 80%; width: 80%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/circuit_diagram_motor_control.jpg?raw=true" align="middle">
</div>

# Software

There are two different sections to the software side of this project:

* C code for the PIC32 to drive the motor and receive feedback.
* MATLAB code used for the user interface.

All the software can be found <a href="https://github.com/MikhailTodes/dc_motor_control" target="_blank">here</a>.

The MATLAB user interface was presented as seen below:

<div class="container"  align="middle">
    <img class="one" style='text-align: center; height: 80%; width: 80%; object-fit: contain' src="https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/user_interface.png?raw=true" align="middle">
</div>
