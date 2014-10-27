---
layout: portfolio_entry
title: Step 6 of HybridV2- Software
tags:
- hybrid
- v2 hybrid
---

##Compiler

One of the highest things on the list to change from version 1 & 2 of the hybrid it is the choice of microcontroller platform. And its not because the Microchip hardware is poor, the units are powerful with great variety and a lot to offer. The main problem is software support. While many other microcontrollers have great UNIX development support, the Microchip software seems stuck in the windows days. Recently Microchip did release Unix support via their compiler; however, as of now the hybrid is currently written for and compiled using the CCS Microchip compiler. For version 3 of the hybrid, the switch will be made to at least another compiler.


<br>
<div style="text-align:center"><img src ="../../img/Code.png" /> <br> <b>Code</b></div>
<br>

##PID Controller

The software is not overly complex. The majority of the program is spent getting and setting the inputs and outputs. There are some checks performed to make sure that the voltage stays between acceptable limits, that the unit stops if a fault is detected, etc. The majority of the work is done in the Proportional Integral and Derivative Controller ( PID) which should be familiar to even the most basic Control Theory students. The PID controller takes in as input the vehicle speed and the users throttle input, the delta of which is the error signal. The unit sets the output of the ICE and the electric vehicle system based on the error signal.
