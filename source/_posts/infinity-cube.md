---
title: Infinity Mirror LED Cube
categories:
  - projects
date: 2022-04-28 11:52:02
cover_image: 2022/04/28/infinity-cube/infinity-cube.gif
---

# Infinity Mirror LED Cube Project

Have you ever seen something cool on the internet and had a burning desire to recreate it? Well that's what happened here when I saw the video below.

{% mp4gif inspiration.mp4 %}

**Design**

Before starting the sketch I figured out what LEDS to use. I wanted high density LEDS so I settled on WS2812B individually addressable LED strips that had 60 LEDs per meter which worked out to 1.66 cm per LED. I chose to have 8 LEDS per side, so that it was an even number and easy to use in code. The LED strip had a width of 1 cm. Knowing this information, I could finally start the sketch.



Length of 13.50 
With the sketch done I started designing the cube in Fusion 360, which is the CAD software I was the most familar with at the time. The cube consisted of two parts, a top piece and a bottom piece to make printing easy.

{% asset_img post-image 'cad-bottom.png' %}

An important consideration was the wire routing, since the LED strip needed a continuous data wire running through the whole strip. To solve this issue, I designed a channel that runs through the cube's walls from one corner to the opposite corner. 

{% asset_img post-image 'cad-top.png' %}


**Assembly**

{% asset_img post-image 'laser-cut.webp' %}


**Final Product**


{% mp4gif final-cube.mp4 %}
