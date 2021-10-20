---
layout: post
title:  "Physical Computing: Week 3 - Tone Output & Servo Motor Control"
author: isaiah
categories: [Phyiscal Computing]
image: assets/images/flatbed.jpeg
featured: true
---

## Summary

Being that I love music and sound, the tone output lab is my favorite lab thus far. By completing this lab, I was able to dive into the different capabilities of how tone output can be used in future projects. As far as the servo motor control lab, that was a different story. The setup for this lab took me a bit longer than the tone output lab, considerably due to readjusting the header pins attached to the motor itself. Unfortunately, my motor was not pulsating as expected but I was able to identify why this may have been. So let's get into it!

## Tone Output

### Setup: 

[comment]: <> (Picture here)

For this lab, the setup was fairly easy. The primary, and singular, difference from previous labs was the alligator clips that I used to attach the positive and negative of the speaker to the appropriate digital pin and ground resistor, respectively. 

### Code & Demo:

This block of code checks the sensor input range by initializing serial communication and printing out the corresponding values from the analog input reading.

[comment]: <> (Picture of code here)

This block of code checks to see if the speaker works by playing a single tone continuously. The tone() function generates a square wave of the specified frequency (440). The pin number, frequency and duration are the parameters, in order. Here is a video of this example demonstrated:

[comment]: <> (Video here)

[comment]: <> (Picture of code here)

This block of code takes the sensor reading, maps it, and then plays the tone according to the mapped frequency. 

[comment]: <> (Picture of code here)

This block of code is a bit more complex ; it ultimately plays a melody by using diffeent notrs from a library, "pitches.h." Here is a video of this example demonstrated:

[comment]: <> (Video here)

As a side note, the musical instrument part of this lab will be my first class project, stay tuned.

## Servo Motor Control

### Setup:

[comment]: <> (Picture here)

This setup was a bit annoying at first, I must admit. The header pins had to be adjusted so that it can properly stay attached to the wires on the motor. It probably took me up to 20 minutes but once I watched the reference video, everything clicked (literally and figuratively).

[comment]: <> (Picture of code here)

This block of code introduces the Servo library, which has many functions that help with programming any Servo motor. I created an instance of the servo object to access specific member functions of the servo. Then, I attached the pin to the servo and map the sensor reading which was used to pulsate the motor at the specified angle.

In short, it did not work for me. After investigating and hypothesising, it is safe to assume that I could have used a different sensor (potentiometer) which was also used in the reference video. 

## Takeaways

* Whenever stuck, ALWAYS refer to any reference videos that further explain the concept and can properly demonstrate the lab.
* When it comes to proper volume for tone output, transistors are vital.
