---
layout: post
title: 'Watch Dogs Inspired Wireless Hacking Drone Using a Pineapple Nano'
published: true
---
<p> Today I finally got around to getting my WiFi Pineapple Drone, Project Cuckoo, out and flying. This was (is) a fun project 
partially inspired by the Ubisoft game, Watch Dogs 2. I say partially, as I've always had an interest in combining my hobby of
infosec/messing with wireless security, and my other hobby of UAS/drones. </p> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/lKtKYhTO5wk" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<p> Project Cuckoo is so named, because of the nature of the Cuckoo bird. Cuckoos are birds that will lay their eggs in other 
birds' nests, and then fly off leaving the nest's owner to incubate and care for the cuckoo bird egg. In the same manner, 
Project Cuckoo flies to it's target, lands, and is a rogue access point/pivot for getting into the targeted network. You then 
drop your (egg) shells/persistance, and fly off. Thus, the silly name Project Cuckoo </p> 

<p> At it's core, Project Cuckoo is a pretty average platform, with a couple of special features. It's hardware consists of a 
Betaflight OMNIBUS F4 Pro V2 Flight controller, M8N GPS, DYS F20A ESC, 2006 2400KV motors, and 5030 carbon fiber 2 blade props, all mounted 
to a 3d printed ABS frame of my own design. </p> 

<p> Now about those special features. The DYS F20A ESC has an integrated 5v buck converter. To this, I connected a panel mount 
female USB plug, which is mounted in the lower section of the frame. This powers the Hak5 Pineapple Nano, without any modfication.
The other interesting feature is the power source. I'm using LG HG2 cells to power the drone. They are safer, and have <b>MUCH</b> 
higher power density than any current lithium polymer chemistry. They have sufficient current to make the platform move and react
pretty quick too. There is however one issue I'm facing involving the voltage curve of lithium ion vs lithium polymer, and I go 
into more detail and potential resolutions in the article <b>here</b> (not yet posted). However over all, I'm pretty happy with 
the duraiton, handling, and form factor of these cells. </p> 

<p> At the end of the day, Project Cuckoo was created to have fun, and show what's possible. It's not perfect, and I still have 
changes and optimizations to make, but it's functional. It could happily fly and land somewhere it probably shouldnt be, and 
conduct electronic surveillance or even active attacks against wireless networks. The technology is here to stay, and it will 
ultimatley be an issue faced as we go forward. This is just one of many uses for UAS that should be considered and thought about in modern security,
both network and physical. </p> 

<p> Massive thanks to Darren from Hak5 for supplying the Pineapple Nano for this project. It's a great piece of hardware and I encourage anyoen interested in wireless security to check it out. It makes for great demonstrations that are easy to grasp. 
[More info on Pineapple Nanos here](https://www.wifipineapple.com/pages/nano) 
<p> I will likely continue developement on this concept, refining it and increasing it's feature set and capabilities. I currently
do not have plans to produce more of these platforms, however I am considering it. </p> 
