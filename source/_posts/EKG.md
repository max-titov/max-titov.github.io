---
title: Electrocardiogram
categories:
  - projects
date: 2023-12-08 07:59:04
cover_image: 2023/12/08/EKG/board.png
---

# Electrocardiogram Project 
**ECE Fundamentals III (ECE3750) Final Project**
**Made by Max Titov, Quentin Olsen, and Bhargav Moosani**


**Project Overview**
The goal of the project was to create a functional electrocardiogram (EKG). We designed five electrical subsystems, with each team member taking on specific responsibilities. An example of a recorded pulse can be seen below:  

{% asset_img post-image 'filtered-output.png' %}

<br/>The electrical pulses from a subject's wrist were processed through an in-amp and integrator system, followed by a filter to remove high frequencies. The filtered signal then passed through an isolator for protection against electrical failures, and finally underwent digital signal processing for a clean output. The signal path can be seen in the diagram below.  

{% asset_img post-image 'diagram.png' %}

<br/>There were five electrical subsystems: power supply, instrumentation amplifier, anti-alias filter, and the isolator. They are described in detail below.  

**Instrumentation Amplifier**

The point of the power supply is to set VCC, for which most integrated circuits on the board will use, to 3.3V. This is implemented with two different sources. The first is done by stepping down a 9V voltage from an auxiliary battery, using a voltage regulator (U6). The second from the Analog Discovery 2’s DC voltage supply. This directly puts out 3.3V and allows isolated system tests.

{% asset_img post-image 'in-amp.png' %}
<br/><br/>

**Anti-alias Filter**

The anti-aliasing filter seen below is a 4th order Butterworth filter, which is used to attenuate high frequency signals and prevent as much rippling as possible in the pass-band. The filter is made up of two cascaded 2nd order low-pass filters. Since our filter’s total response is 4th order low-pass, we’ll have a -80dB/dec roll-off in our frequency response at the corner frequency.

{% asset_img post-image 'filter.png' %}



{% asset_img post-image 'setup.png' %}


{% asset_img post-image 'output.png' %}



