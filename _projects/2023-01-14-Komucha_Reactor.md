---
title: 'Kombucha BioReactor'
subtitle: 'Independent Study - Living Matter Lab ATLAS Jan 2023'
date: 2023-01-13 12:00:00
description: Building a BioReactor to grow and monitor the lifecycle of Kombucha
featured_image: '/images/booch_image.png'
---
## The Reactor

Due to my interest in joining the <a href="https://www.colorado.edu/atlas/living-matter-lab"> Living Matter Lab </a> as a PhD Student next fall, the Director of the lab, <a href="https://www.colorado.edu/atlas/mirela-alistar">Dr. Mirela Alistar</a> and <a href="https://www.colorado.edu/atlas/fiona-bell"> Fiona Bell</a>, a PhD candidate in the lab, were kind enough to let me help out on some work they're looking to wrap up, allowing me to expand my portfolio of designing applications for lab research findings.  One of those projects, after much deliberation, was to create a Kombucha BioReactor, a device that monitors as well as interacts with the observer, allowing the observer to hear changes in the lifecycle of the organism.  Right away, I was sold on the idea and excited to dive in.  In the spirit of final product first, here you go:
<p align="center"><img src="/images/boochReactor.png"></p>

## Background and Inspiration

Due to the often limited resources of labs and the nature of academia, available sensors and equipment are not always what you expect or desire.  In our case, we were able to procure an Si7021, TSL2561, and a photocell, which was enough capability to allow for the purposes of the build.  After reading documentation from SparkFun on their devices, I was off to the races.  Or so I thought... (he said ominously..... Insert SFX here!)

The other main consideration was how to relate this iteration of a BioReactor into something familiar enough to be relatable to prior research but capable enough to provide additional datapoints for continued research.  In the end, we decided to use a mason jar with an acrylic lid and a laser-cut box to hold the components below the device.  Alluding to the previously ominous comment, this was the easy part of the build and took less than 2 hours to construct, including finding materials and writing the code to build the box.

## "Plug-n-play" sensors, an I2C Bus, and a kid's journey to figure out why they dont work as advertised...

As I've only worked with non-SDA/SCL dependent sensors in the past, or was able to only use a single device on a build instead of multiple, I had no idea how much of a headache I was walking into for the Si7021 and TSL2561 sensors from Sparkfun but set off to get these sensors sending data over the terminal as quickly as possible.  Frankly, the documentation is quite dated on these sensors and not entirely helpful. Although the walkthroughs are generally quite helpful, the walkthroughs on these sensors were quite the opposite - no issue getting a sensor to work on its own, but use the I2C bus information provided by SparkFun and you were going nowhere fast.  Thankfully, with the help of <a href="https://www.colorado.edu/atlas/mary-etta-west">Mary Etta West</a>, my guardian angel and a PhD student at ATLAS, we were able to get the code to work to integrate the sensors on the bus.  Lesson learned from this project?  Always have a former SparkFun engineer by your side when things get tough.

Here is how it's all wired up!
<p align="center"><img src="/images/boochSchematic.png"></p>

Wiring Diagram of the build.
<p align="center"><img src="/images/reactorInnards.png"></p>

After labeling each wire and wrapping in shrink-wrap, they were fed into the box and connected to the breadboard within.

## Sensor Setup

The sensors themselves are hot-glued to the top of the acrylic lid, with the light sensor directed directly downward to monitor light intensity on the scoby itself.  The temp/humidity sensor was angled toward the jar lid and protected as much as possible from any moisture exposure.  Both sensors have hot glue covering wire connection points to help minimize corrosion as well.  
<p align="center"><img src="/images/reactorLid.png"></p>
The photocell itself is hot-glued to the lid of the box to keep it stable while reading changes in light intensity.
<p align="center"><img src="/images/photocellLid.png"></p>

## Discussing Code

For all of you code nerds out there, and for those looking for a how-to on getting a BioReactor of your own up and working, check out the Repo <a href="https://github.com/starbuck10/BoochReactorRepo">here</a>.  The code is pretty straightforward, the only exception being the mapping for the speaker and the tone.  When I was building the project, I noticed very little movement in the values the photocell was printing to the console, so I increased the resistance to 100K from 10K and adjusted the mapping range of the sensor.  I highly recommend you do this as well for your future builds.  The frequency range can certainly be adjusted as well.

## Final Work

After two weeks of bashing my head against the wall to get the code to function properly, here it is!  The final Kombucha BioReactor:

<iframe width="560" height="315" src="https://www.youtube.com/embed/rLRUNepp9hU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Final Image with Scoby, coming soon!