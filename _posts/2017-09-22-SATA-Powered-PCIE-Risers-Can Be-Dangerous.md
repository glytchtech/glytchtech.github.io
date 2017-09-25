---
published: true
---
![Melted Sata Connector]({{site.baseurl}}/images/2017/9/Capture.PNG)
<p>Or rather, the connectors can be. It's common knowledge that molex powered risers in multi GPU rigs (used for things like machine learning and mining) can cause problems, and even start fires. SATA powered risers are recommended over molex, however I've had a number of issues with these as well. In this post, I will make a case for why 6 pin PCI powered risers are the better choice over both SATA and molex powered risers.</p>
<p>The PCI-e specification allows for 75w to be drawn off a 16x PCI-e slot. This isn't an exceptional amount of power, but it is plenty to cause problems with inadequate wire gauge and incomplete/incorrect crimped connectors (as are often found in cheap power adapters.) The most common use for SATA connectors, and even prior to that, 4 Pin molex connectors are to power hard drives. Hard drives draw relatively miniscule amounts of power, so most adapters are produced with that in mind. On the other hand, 6 pin power connectors are most commonly found powering larger GPUs. This raises the bar on both wire gauge and crimp quality, while also spreading the load among 3 pairs of wires and crimps, decreasing the load seen by any one wire or crimp connector significantly, leading to better reliability and safer operation.</p>

<p>Furthermore, 6 pin connector powered risers only require 12v input, and contain an onboard buck converter for the card's 5v needs. This further simplifies wiring, making high powered multi GPU rigs cleaner, safer, and more reliable.</p>

<p>Below are some pictures of my failed SATA power connectors, leading to my SATA powered risers, as well as a picture of the new 6 pin powered risers with integrated buck converter. Beyond that I have embedded a video documenting in some detail, my experience with SATA powered risers and my switch to 6 Pin risers.</p>

![Burnt SATA Riser Connectors]({{site.baseurl}}/images/2017/9/Burnt%20SATA.JPG){ width=50% }
![New 6 Pin Powered Risers]({{site.baseurl}}/images/2017/9/6%20Pin%20Risers.JPG){ width=50% }

<iframe width="768" height="432" src="https://www.youtube.com/embed/9iDw9Y3EcO8?rel=0" frameborder="0" allowfullscreen></iframe>
