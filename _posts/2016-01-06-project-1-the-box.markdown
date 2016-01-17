---
layout: post
title:  "Project #1 - The Box"
date:   2016-01-06 21:10:00
categories: projects
description: My first real project - a box with a magnetic lock controlled by a RFID reader and a permanent electromagnet. New cards can be added by first swiping an Add-card. 
relative-image-url: /assets/nano200.png
---

My first project is a box with a magnetic lock controlled by a RFID reader. 

<div class="video-container">
<iframe src="https://www.youtube.com/embed/lzfL9Y77STQ" frameborder="0" allowfullscreen></iframe>
</div>

The hardware
------------

I started out with Arduino Yun but quite quickly a replaced the Yun with the smaller Arduino Nano. Beside the Ardoino Nano I have used the following components for this project.

* [RFID reader]
* [12v permanent electromagnet]
* [N-channel MOSFET]
* [Diode]
* [Micro switch] 
* RGB led 

There are a couple of reasons for selecting a permanent electromagnet instead of a normal electromagnet. With a permanent magnet you dont have to supply power to the magnet when the box is idle (closed) which of course makes it consume less power and the box also appears "locked" even when the power if disconnected. Another reason is that the magnet becomes quite warm when the power is on.
 
The mosfet is used to control the power supply for the 12v electromagnet and the microswitch is used to make sure that the power to the magnet is on whenever the lid is open, otherwise the box would turn in to a finger guillotine. It's been a long time since I used a transistor and after googling for similar projects I found this [blog post] that described the mosfet and how to use it. 

Finally I mounted and soldered everything on a small board and before it was installed in the box, the finished product looked liked this. 

![Finished product]({{ site.url }}/assets/project-1-board.jpg)

The code
--------

Here you can find the [code]. I know It needs to be cleaned up and refactored and in the project there is also an unfinished implementation for another RFID reader. I plan to cover this and the factory pattern I used in a separate post, when I get it to work...

Images
------
The finished product

![Finished product]({{ site.url }}/assets/project-1-finished-product-1.jpg)

![Finished product]({{ site.url }}/assets/project-1-finished-product-2.jpg)

![Finished product]({{ site.url }}/assets/project-1-finished-product-3.jpg)

The hardware before it was mounted in the box

![Finished product]({{ site.url }}/assets/project-1-hardware.jpg)

The hardware installed in the box

![Finished product]({{ site.url }}/assets/project-1-mounted-arduino.jpg)

The lock is a permanent electro magnet (300N). You can also se the micro switch that makes sure that the current is on whenever the lid is open. Otherwise the magnet will close the lid quite fast....

![Finished product]({{ site.url }}/assets/project-1-open-lid.jpg)


[code]:https://github.com/pstigenberg/RfidMagneticLockApp
[blog post]:http://bildr.org/2012/03/rfp30n06le-arduino/
[12v permanent electromagnet]:http://www.conrad.se/Permanent-magnetisk-Intertec-ITS-PE3529-12VDC-%2a-12-V%2fDC-M5-300-N.htm?websale8=conrad-swe&pi=506163&ci=SHOP_AREA_83990_0214811
[RFID reader]:http://www.kjell.com/se/sortiment/el/elektronik/arduino/moduler/rfid-lasare-for-arduino-p87911
[N-channel MOSFET]:http://www.electrokit.com/fqp30n06l.49374
[Diode]:http://www.electrokit.com/bb809-do41-30v-20ma.44945
[Micro switch]:http://www.kjell.com/se/sortiment/el/elektronik/elektromekanik/strombrytare/mikrobrytare/superminiatyrbrytare-p36054





