---
layout: post
title:  "Physical Computing: Week 10 - Controlling DC & Stepper Motors with a H-Bridge"
author: isaiah
categories: [Phyiscal Computing]
image: assets/images/stepperMotor.jpg
featured: true
---

## Summary
Motion and mobility, I find, are two aspects of physical computing that encourage more interactivity in your project and I am excited to see how I can use it in the future! For this week's lab, I worked with a DC and stepper motor and learned how they can be useful in creating fun projects. Although they were fun to get accustomed to, they also caused me multiple headaches during the circuit setup process. All in all, this process was a great experience so let's take a look.


## Controlling DC Motor with a H-Bridge

### Setup: 

[comment]: <> (Picture of setup here)

This setup is the final product after multiple tries at a working circuit. At first, I tried to the use the mentioned setup without the additional power supply and jack. The DC motor I used for this lab was a 3-6 voltage motor and is compatible with the USB power supply of the Arduino. However, I did not have a few things set up properly which derailed my progress for a while. I realized through additonal helping hands that the 5 voltage chips on the back of the Arduino were sodder together which inevitably did not drive enough power to the motor connected to the H-Bridge. I also did not have the VM (motor voltage supply input) connected to the power bus. Lastly, I had initially connected the capacitor to the power and ground bus but understood, after the fact, that the capacitor is only needed to smooth out possible voltage dips when the motor turns on. After correcting these mistakes, I was able to have a proper setup for a working motor.

### Code & Demo:

This block of code sets up constants for the switch pin, the two motor driver pins, and the PWM enable pin of the motor driver. 

[comment]: <> (Picture of code here)

This block of code sets all the pins for the motor driver as outputs, and the pin for the switch as an input. Then sets the PWM enable pin high so the H-bridge can turn the motor on.

[comment]: <> (Picture of code here)

This  block of code reads the switch. If it’s high, it turns the motor one way by taking one motor driver pin high and the other low. If the switch is low, it reverses the direction by reversing the states of the two pins.

[comment]: <> (Picture of code here)

Here is a video of this being demonstrated:

[comment]: <> (Video here)


## Controlling Stepper Motor with a H-Bridge

### Setup:

[comment]: <> (Picture of setup here)

This setup was not fair at all, to say the least. The lab primarily showed schematics for a separate H-Bridge circuit connected to different Arduino versions that did not include the Nano. I tried to follow the schematics with similar connections to the H-Bridge circuit that I used but the stepper motor was unsuccessful in turning on. Let's get into the code to see what the stepper motor was supposed to do.

### Code & Demo:
[comment]: <> (Picture of code here)

This block of code runs the stepper motor through the H-bridge using the Stepper library. It runs the stepper one step at a time, to see that all the wires are connected correctly. If they are, the stepper will step one step forward at a time, every half second.

[comment]: <> (Picture of code here)

This block of code makes the stepper move one whole revolution at a time.

Assuming that my setup is faulty in its circuit connections, I was not able to capture a video of a working stepper motor but I hope to troubleshoot this in class with answered questions


## Questions & Takeaways
