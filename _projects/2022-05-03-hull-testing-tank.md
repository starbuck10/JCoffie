---
title: 'Project: Pier Pressure'
subtitle: 'A proof of concept for rapid boat hull design prototyping'
date: 2022-05-03 06:00:00
description: Developing a proof of concept for rapid boat hull design prototyping using Arduino
featured_image: '/images/expoTank.jpg'
---

## Project Purpose

The purpose of the project was to develop a rapid prototyping and testing setup that allows for the development and testing of innovative vessel hull design and oceanic advancements that help reduce dependency on fossil fuels - the overall goal of the project is to develop a new advancement in this arena.  The driving force behind this project is to contribute to the effort in reducing the effects of global warming and to encourage the industry to use creative technologies to reduce the cycle time required for new hull designs to hit the market.

---

## Problem Statement

<p align="center"><img src="/images/hullSlide1.jpg"></p>

By 2050, over 570 low-lying coastal cities will face projected sea level rise by at least 0.5 meters, putting more than 800 million people at risk from the impacts of rising seas, extreme weather and storm surges.  Further, the planet's average surface temperature has risen about 2.12 degrees Fahrenheit (1.18 degrees Celsius) since the late 19th century, a change driven largely by increased carbon dioxide emissions into the atmosphere and other human activities, creating a massive amount of strain on our oceans and the planet as a whole.

<p align="center"><img src="/images/hullSlide2.jpg"></p>

As the cost of fossil fuels, and the effects of their usage, become more difficult to bear, companies and organizations will continue to develop newer technologies that can assist in removing fossil fuels from the global warming conversation.  For instance, cargo ships are now being fit with sails to allow them to transit the trade winds with less fuel consumption.  Our hops is that by creating a low-resolution prototyping system that allows iteration in days instead of years, we can assist boat designers and builders in determining more efficient design, which we hope will propagate into the designs of less complicated, and less expensive craft on the water (villages, personal watercraft, etc.).  

---

## Project Background

The project was designed to be split into two parts: 1. Creating 3D printed boat hull designs and innovating around the technology present and 2. Building a testing facility that will determine the effectiveness of those technological improvements.  Due to the complexity of this project, the initial prototyping and project design was split by myself and Abdulaziz Maiyouf, who worked on the testing tank portion of the project.

The goals of the project were as follows:

1. Design low-cost hull design
2. Identify areas of technological opportunity in design
3. Test those opportunities
4. Identify low-cost design that assists in better fuel economy
5. Develop a report to denote findings and areas of future research

Note: Throughout the project we realized the need to focus on baseline testing and not on the development of future hull designs, leaving that component of the project for future development.


---

## Design

The best overall hull design is a question of form and of function - developing the most functional craft that doesn’t draw the user into the form is just as ineffective as a beautiful design with no function.  For the purposes of this project, the design took into account overall cost to build, the likelihood of adoption of new designs and technology, as well as attempting to prototype designs that are familiar to those that already live in the world of naval design.  For instance, a completely new multi-hull design is not the most effective use of our time whereas adjustments in friction, lift, and reducing drag would be a better use of our time.

There are two initial designs that I’ve built using my Ender v3 that will be used for a baseline with one of the designs presented using different sizing and a removal of the keel and rudder to use for reference data.  The first hull is a racing sailboat hull, designed to be sleek and to provide the least amount of resistance to the waters’ flow past the hull (see figure 1).  The second hull design is a cruising sailboat, most common among amateur and professional sailors for their combination of speed, carrying capacity, and comfort (see figure 2).  This hull was also scaled down and the keel and rudder removed for reference as a third testing hull.  

<p align="center"><img src="/images/hull1.jpg"></p>
<p align="center">Figure 1: Racing boat hull</p>

<p align="center"><img src="/images/hull2.jpg"></p>
<p align="center">Figure 2: Cruiser hull 1 & 2</p>


Following the initial tests, it become apparent that adding additional hulls to validate data, and to use as a reference for the hulls mentioned above, was essential.  The two additional hulls selected for use are a scaled down freighter with a bulbous bow and a working crane ship with little to no technological advancements, see figure 3 and figure 4 respectively.

<p align="center"><img src="/images/hull3.jpg"></p>
<p align="center">Figure 3: Freighter with bulbous bow</p>

<p align="center"><img src="/images/hull4.jpg"></p>
<p align="center">Figure 4: Working Ship</p>

The overall design of the project began with a simple illustration showing the interconnected components of the build, heavily reliant on an Arduino to measure the flex in the flex sensors and leveraging the serial port to retrieve the data.

<p align="center"><img src="/images/projDesign.jpg"></p>
<p align="center">Figure 5: Illustrative example of project design</p>

---

## Assessing the Project

Assessing the project is the second part of Project Pier Pressure and it leverages a testing tank, an Arduino, and a series of flex sensors.  These flex sensors, located aft of the hull, will measure the turbulence that passes pass the hull direct aft and on the port and starboard sides.  This turbulence is a measure of the anticipated drag that a hull will create (similar to wind tunnel testing for automobiles) and the less variance in turbulence the better.  Before we can determine the anticipated performance of different hull shapes and designs, a baseline will need to be calculated with the current hulls while telltales are used to visually determine the direction of current and potential of eddies present in the tank that might affect the readings.  Overall, this project is a proof-of-concept demonstrating the possibility of using 3D printed hulls in boat development so the data analysis will be used in future iterations of development.

---

## Putting it all Together

The goal of this project is to provide an innovative testing process for new hulls that minimizes the amount of time traditionally required for new developments.  By leveraging 3D printing and an Arduino testing tank, we’re looking to see if this process will speed up the innovation process and put new technological designs in the hands of boat builders before climate change permanently changes our oceans and waterways.   For this project, the following books were used as a reference for determining the best way to design a testing tank and which technological improvements would provide a proper baseline for testing the effectiveness of this project:

1. Wandering Under Sail by Eric Hiscock,
2. The Architect’s Apprentice: The Story of the Design and Construction of a Wooden Sailboat by Gary Schwarzman,
4. Understanding Boat Design, 4th Edition by Ted Brewer, and
5. Theory of Naval Architecture by A.M. Robb

---

## The Results

The results of the project demonstrate that the most effective hull design tested for baseline was the freighter, as this hull design had the least amount of variability in the flex sensor angle changes.  These results show that the flow around the freighter’s hull remained the most consistent of the tested hulls, demonstrating the effectiveness of water displacement while it’s in motion, which can be most likely attributed to the bulbous bow and the early transom design that minimizes turbulence astern.  

<p align="center"><img src="/images/graphs.jpg"></p>
<p align="center">Figure 6: Flex Sensor angle (y-axis) over time for differing hull types</p>

---

## Lessons Learned and Areas for Improvement

As with any project, there are a myriad of areas for continual improvement, particularly in the next iteration of design and development.  Here are a couple of things that should be addressed in that next iteration:

1. 3D printing setup - I spent quite a bit of time customizing my Ender v3 as the low entry cost of the setup often leads to subpar or underperforming prints.  Read: The numbers of times I wait hours to find a messed up print at the end was infuriating.  I ended up using direct drive and auto-bed leveling upgrades to help with the prints and I found the consistency was quite helpful, along with some bed glue.  For anyone looking to continue this work or create a similar project, I highly recommend making sure your machine is equipped to handle what you need it to in order to avoid undue frustration.
2. Tank sizing and using tell-tales - Our tank is a bit small as demonstrated by the tell-tales we installed on the tank - these changed direction in the back corners of the tank which shows us that flow wasn’t as circular as we had hoped.  By inserting some clear plastic to direct flow or by increasing the tank size, we could leverage the wave action in a positive manner instead of fighting against it for readings.
3. Motor and testing environment -  The last major improvement we’d recommend is 3d printing a nozzle on the motor that disperses the current more evenly across the hull - the direct water flow was a quite strong current and didn’t allow a natural flow to occur in the tank.

<p align="center"><img src="/images/waterTank.jpg"></p>
<p align="center">Figure 7: Overall tank with tell-tales in place</p>

---

## Parting Thoughts and ATLAS EXPO 2022

As the culminating point of the project, Abdulaziz and I presented out work at ATLAS EXPO 2022 where we received lots of positive feedback, coupled with ideas for continued development.  Here are a couple of those thoughts from exhibitors:

Know your audience - living in Colorado, this type of display was a new experience for most exhibitors as the ocean isn’t really in our backyard.  We were asked throughout the presentation what the product was designed for and although this is more of a personal passion for me, the point is still valid - be sure to provide visitors with a thorough understanding of how this project can make an impact.
Interactivity - this project has a bit of interactivity due to the ability to switch out hull designs and see the change in the lice serial plotter feed.  In the future, waterproofing the technology to allow a seamless experience would be ideal
And finally, expect people to be passionate about your project when you’re passionate - I had a number of sailors come up and comment on how this tech could be used in the future and the comments of “You’re going to be rich one day!” was a wonderful way to end the day.

<p align="center"><img src="/images/expoTank.jpg"></p>
<p align="center">Figure 8: CU Boulder ATLAS EXPO 2022 Display</p>
