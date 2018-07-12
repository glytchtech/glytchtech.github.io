---
published: true
---
Recently I've been working on a custom DDL (Digital Data Link) for my various drone projects. Requirements were multiple telemetry streams, one for the flight controller and one for any custom payload, as well as  HD digital video. Minimum 1 mile of range, conservatively, and I wanted it to be almost entirely self contained, with only a display device being external. I believe I have accomplished those goals, with this system.
![Dh2i0-hXcAIcpsN.jpg]({{site.baseurl}}/images/2018/7/Dh2i0-hXcAIcpsN.jpg)

I've chosen to use <a href="https://github.com/seeul8er/DroneBridge"> DroneBridge </a> firmware to build this system. It is an open source implementation of wifibroadcast that provides extra features and a rather slick Android based app, that connects to the DDL over USB tethering or WiFi. It gives the system a DJI-like interface, with a minimap and OSD with important details. 

In short, Wifibroadcast is a clever system that uses cheap and readily available wifi cards, but without the traditional wifi protocol. Instead the cards are in monitor mode and injecting packets in a unidirectional manner, giving low latency "analog-like" behavior. It has a graceful fall-off as you get to the edge of your range, dropping frames rather than cutting out entirely. Lower bitrates also allow much greater range than traditional WiFi. 

As I mentioned above, DroneBridge can send bidirectional flight controller telemetry, as well as a second payload telemetry stream, configurable to work with almost any serial based system. The DroneBridge firmware also supports RC stick inputs on the ground via a sim cable, and will send that over the link too. Encryption is also possible, enabling a single relatively secure data stream, unlike most hobbyist, consumer, and commercial systems these days.  

So now that we've covered the firmware and understand that it meets my requirements, let's talk about the hardware and my requirements for such. 

As stated above, I wanted something compact, mostly self contained, and capable of minimum 1 mile range in reasonable conditions. I've modeled the system on Aeroviroment's (a defense company that produces a variety of drones and related systems) DDL, or digital data link. It is a small box, that is externally powered and allows similar capability (though with proprietary software, I'm sure.) 
This was a good start, but being externally powered adds points of failure and increases overall system complexity. 

My system is made up of a 3d printed housing, in which a a Raspberry Pi Zero, Alfa NEH wifi card, USB hub, and an NCR18650B battery cell with associated circuitry reside. All but one of the ports on the USB hub were desoldered, as well as the port on the wifi card. These are then soldered directly together with  short lengths of wire. This was done to make the system more compact and integrated, as well as more reliable. The NCR18650B battery should allow somewhere between 2 and 6 hours of run time, dependent on conditions. More formal testing will be done soon. There is a small board which allows micro USB charging, a boost converter then boosts the voltage from the battery, to the requried 5v system level.  Soon there will be 2 LEDs to indicate power on and system status. 

I also intend to add a secondary small internal wifi dongle, which will allow a wireless connection to the box, allowing more system flexibility. 

![Dh2i1-eWsAAyfyz.jpg]({{site.baseurl}}/images/2018/7/Dh2i1-eWsAAyfyz.jpg)

Some other neat features of DroneBridge are that  it supports dual air side cards, and 4 or more ground side cards for true diversity, allowing several different antennas to be switched between automatically and seamlessly. For example, a few directionals facing different directions, with an omni at the middle for close range. It really is quite awesome firmware and is being very actively updated. I plan to make a couple different versions of these boxes based around it,but this is the most compact version I have in mind, at least for the moment.

Configurations are pretty versatile. A compact, quickly deployable tripod allows better range for light GCS setups. It can be secured internally or externally to bags, belts, and vests for truly portable/on the move operation. Wired and soon, wireless interfacing to phones, tablets, and laptop/desktop computers. Also direct HDMI out and recording to USB flash drive is possible. Ground station software like QGroundControl is gaining more support by the firmware, DroneBridge, and new features being added.
Like I said, it's pretty slick and self contained. 

![Dh3DMxdWkAIfx29.jpg]({{site.baseurl}}/images/2018/7/Dh3DMxdWkAIfx29.jpg)

One example loadout: I can fit #ProjectCuckoo, several batteries, the charger, an X-Lite controller, this custom DDL, a compact tripod, a tablet/GPD Pocket, and more in the Hak5 Tactic Elite Bag, allowing for a rapidly deployable, 1 person operable, HD video streaming and wifi pentesting drone platform.
The entire kit weighs under 10lbs, 3 batteries would provide upwards of an hour of flight time, 1+ mile  range, and not to mention on-station 'perch and stare' time, which still needs testing.
You really can't get more capability in this kind of package. 

This system, integrated with #ProjectCuckoo, will be on display at the Hak5 booth at Defcon 26. At this time, I'm unsure if I'll be able to have it powered up and displaying video. I do want to do some testing though, as I'm curious as to what the ISM band hellscape there will do to it. 
