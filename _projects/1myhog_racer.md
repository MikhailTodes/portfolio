---
layout: project
title: MYHOG Racer (coming soon)
date: Feb, 2016
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/myhog_mak1.jpg?raw=true
---

# Abstract
MYHOG racer stands for Myo Controlled Hemispherical Omni-directional Gimballed Racer. It uses just one hemisphere as a drive force. With the hemisphere constantly being spun and making contact with the ground, the gimbal's tilt allows drive in any direction. Because the drive force is a hemisphere, the more it is tilted, the greater the radius between the point of contact with the ground and the central axis of rotation. As a result speed can be easily controlled. (More information can be found <a href="https://en.wikipedia.org/wiki/Hemispherical_omnidirectional_gimbaled_wheel" target="_blank">here</a>). The <a href="https://www.myo.com/" target="_blank">Myo</a> is an armband worn just below the elbow of the driver. It uses a combination of EMG, IMU, and accelerometer signals to achieve machine trained gesture recognition that allows the driver speed and direction control of the MYHOG. 

[comment]: <> (put video here)

# Hardware

### The Frame
The frame is made out of 1/8 inch thick plywood. I used a laser cutter to carve out the design. This made it easy and quick to re-cut any pieces that were needed. 

[comment]: <> (pic of frame design)

The base of the frame and the upright housing the servos, are each 3 pieces of  plywood stuck together with wood-glue and screws. The two supporting pieces (one upright with “MYHOG” carved on it and the joining top piece) are both two pieces of plywood thick. I created the design for these pieces using the free online software, “OnShape”. The Solid Works files for each part can be found <a href="https://github.com/MikhailTodes/myhog_racer/tree/master/Model" target="_blank">here</a>. The different pieces of the frame are designed to fit in firmly with each other. 

At the other end of the frame, I originally attached two caster wheels for support. Since the first iteration I have changed to using ball bearing wheels instead. This allows for better omni-directionality. I have also spread the wheels a bit further out from the centre to help support the frame a bit more. 

[comment]: <> (pic of frame built)

### The Gimbal
The gimbal attaches right between the two poles of the upright piece that houses the sevos. 

[comment]: <> (pic of gimbal design)

The gimbal is made up of two 3D printed pieces. (Solid Works files found <a href="https://github.com/MikhailTodes/myhog_racer/tree/master/Model" target="_blank">here</a>). The inner piece has the motor attached and rotates about the roll axis in the MYHOG's forward direction. This allows for forward or backwards drive. It is driven by the bottom servo. The outer piece rotates about a pitch axis in the MYHOG's forward direction, allowing the MYHOG to steer left or right. It is driven by the top servo. At the moment the servos are connected to the gimbal pieces using small wooden rods. Each rod has a hole in both ends to enable a threaded wire to attach and still allow enough flexibility for rotation. With testing I have found this allows too much play and thus instability. Different materials will be tried in further models. 

### Motor Connection and Hemisphere
The hemisphere is a racquet-ball ball with the top cut off. I 3D printed the piece below to attach to the motor and fit inside the racquet-ball ball. 

[comment]: <> (pic of motor connection piece)

I then filled the hemisphere with glue from a glue gun. Allowing the glue to cool down and harden secured the motor connection piece in place and solidified the hemisphere.

# Electronics

### Motor

### Servos

### MYO 

### Communications

# The Software

### Myhog Ros Workspace

Myo/Joy node

### PIC32 C Code

[comment]: <> (Because the drive force is a hemisphere, the more it is tilted, the greater the radius between the point of contact with the ground and the central axis of rotation. As a result speed can be easily controlled.)