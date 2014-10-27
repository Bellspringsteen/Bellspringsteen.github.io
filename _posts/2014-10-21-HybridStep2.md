---
layout: portfolio_entry
title: Step 2- Input and Output
tags:
- hybrid
- v2 hybrid
---

##Input

  For the bike, the brakes were left alone, and it is only the throttle which was changed to become the input device for the hybrid system. The original Honda Metropolitan had a cable actuated hand throttle that went directly to the throttle valve ( the honda met is a carbureted bike.) On the left hand of the handlebars was added a hall effect sensor throttle which outputs a voltage proportional to the amount it is turned. The hybrid system takes this input in as the user input.
However, instead of a usual vehicle in which the throttle corresponds to how much power the user wants to apply, the throttle instead corresponds to the desired speed of the vehicle a so called speed control throttle. While riding, the effect is not that different, although it does have some unique differences. For instance, in a regular vehicle if you have the throttle half way open and you are cruising down a level street your speed might equalize at sixty miles per hour. If you suddenly come upon a hill, and do not adjust your throttle, you will now be traveling at perhaps thirty miles per hour. In a speed control throttle, when hitting the hill the engine output would increase to maintain sixty miles per hour.
Electric throttle are available from a variety of sites, mostly made for electric bicycles/scooters etc. When choosing, your options seem to be 0-5V potentiometer and hall effect throttles. An earlier iteration of the hybrid used a potentiometer input, but as is cautioned elsewhere on the internet, the throttle wore out quickly and soon developed some terrifying inconsistencies which made riding interesting. That seems to be the reason why most of the electronic throttles are hall effect sensors.

<div style="text-align:center"><img src ="../../img/EletricThrottle.jpeg" /> <br> <b>Electric Throttle</b></div>

  The throttle is the main input. The other two are a power switch, mounted next to the bikes lock, which turns on and off the hybrid system and a bypass switch on the resistor across the main power contactor. The bypass switch is inline with a resistor which loads the electric system controller across the contactor, without the switch the resistor will discharge the capacitor bank over about a week.

##Output

Besides the obvious output of the wheels spinning and propelling the bike down the road, the other outputs from the hybrid system are two meters showing the voltage of the capacitor bank. The first meter is a row of single LEDs which are glued in place above the speedo. The meter functions similarly to a available boost gauge in a arcade racing game, in that it shows you an approximate of how much electric assist you have available. The second output is a cheap analog voltage meter mounted near the right foot, bought from Radio Shack (shocking.) Besides the boost functionality, the other reason to monitor the output is in case something goes wrong and the voltage is allowed to get too high. If the voltage exceeds forty eight volts for the capacitor bank, there will be a mini explosion right under the seat. Not good.

<div style="text-align:center"><img src ="../../img/Speedo.png" /> <br> <b>Voltage Meter above Speedo</b></div>
