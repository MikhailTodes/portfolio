---
layout: project
title: Springboard Dynamics
date: November, 2015
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/springboard_setup.png?raw=true
keywords: Keywords - Euler-Lagrange, Dynamic Modelling, Simulation, Mathematica 
---
## Overview
The purpose of this project was to mathematically model and simulate the basic dynamics of an elastic impact between a diver and a spring board. The simulation was done in Mathematica using Euler-Lagrange principles.

## Code
This was modeled using Wolfram's Mathematica software. The code can be found <a href="/portfolio/public/pdfs/springboard_code.pdf" target="_blank">here</a>.

## Explanation of the code  
The first section of the code contains the transformations to describe the different coordinate frames used in the modeling. 

Some functions are defined for later use. There are also some parameters set that can be adjusted for different results, eg. spring coefficient, gravitational acceleration, mass of the diver, mass of the board, length of the board, etc.

The Lagrangian equation is setup using the difference between the combined kinetic energies and the combined potential energies.

The next section of code simulates the pre-impact model of the system. Here initial conditions can be set, eg. the initial position, orientation, and velocity of the diver. 

After that comes the impact section of the code. Here the constraints are defined as to where the impact takes place. Then using the impact update equations the new *initial* conditions are set. This allows for the post impact simulation of both the diver and springboard.

The last part of the code is used for plotting results and the animation of the simulation as seen in the video below. 
 
## Simulation Video
<iframe width="420" height="315" src="https://www.youtube.com/embed/MVjevcx9t08" frameborder="0" allowfullscreen></iframe>