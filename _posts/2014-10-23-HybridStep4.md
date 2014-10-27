---
layout: portfolio_entry
title: Step 4 of HybridV2- Electrical
tags:
- hybrid
- v2 hybrid
---

##Super Capacitors

The super capacitor bank is built of three of these units in series. The hybrid version 1 used individual Maxwell units built into a custom pack. While great units, building up the modules proved to be a great deal of work and concerns over the structural integrity, especially with the flexing of the motorcycle frame, mean that version two uses prebuilt modules. However, because the size of the unit is constrained it limits how many units can be stuffed into the frame. Version 3 will most likely go back to using individual Maxwell units.


<br>
<div style="text-align:center"><img src ="../../img/ElectricSystem.jpg" /> <br> <b>SuperCapacitor Bank</b></div>
<br>


##Electric Controller

While the hybrid unit controls the overall system, the direct powering of the electric hub motor is controlled by an off the shelf controller. Specifically the controller is a Kelly eBike Controller with details here. The unit could be replaced with almost any brushless dc controller; however, for the price I have found them to be OK units. In the future, I would want to combine the hybrid control unit with the electric motor controller. The controller is mounted on the aluminum spar which connects the ICE to the hub motor. The inputs to the unit are configured for a throttle input, brake input, and a brake switch. This presents a few complications as the hybrid unit is what is driving the unit. Instead the hybrid unit outputs analog voltages and closes switches in order to mimic a drivers actions and to drive the electric controller.

##Others
Besides the hybrid unit and the super capacitors, the rest of the items would not be out of place in a regular electric bike. For instance there is the main contactor which separates the high voltage from the controller. In addition there is a thermistor measuring hub motor temperature.
