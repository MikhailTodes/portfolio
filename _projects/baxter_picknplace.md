---
layout: project
title: Baxter Pick and Place
date: December, 2015
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/baxter_final_pose.png?raw=true
---

## Overview
As a final project for the Embedded Systems course I took, we were required to use Rethink Robotics' Baxter for a pick and place application.

##Additional Components

The basic project was to pick up 6 objects and place them in a box on the side. Extra marks were given for the following:

* Picking up different shaped objects
* Picking up different coloured objects
* The speed at which Baxter could succesfully pick and place 6 items.



[//]: # ([Video of End Product](https://www.youtube.com/watch?v=Uo60e5Leo50))
[//]: # (<a href="https://www.youtube.com/watch?v=Uo60e5Leo50" target="_blank">New Tab</a>)

##Video
<iframe width="560" height="315" src="https://www.youtube.com/watch?v=Uo60e5Leo50" frameborder="2" allowfullscreen></iframe>


## Overview
This project was part of the course ME 495, Embedded Systems in Robotics, at Northwestern University. The main goal of this project was to use the Baxter robot to autonomously pick objects off of a work surface and place them in a container. The blocks can be placed at any position and orientation on the table, and they are also sorted by tag number into two groups.

We split the task into four main parts which are implemented through a state machine:

<l>
<li> Locating a block with tags using ar_track_alvar</li>
<li> Moving to above the block position using a joint trajectory</li>
<li> Adjusting the height using a Cartesian trajectory</li>
<li> Grabbing the block and dropping it in a specified position</li>
</l>

All of the code for this project is hosted on [this page](https://github.com/rikkimelissa/baxter_pick_and_place).

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/H4gZ741p81o" frameborder="0" allowfullscreen></iframe>
</p>