One of the many things that limits printing speed is how fast you can go before getting speed/acceleration related artefacts in your prints - one of the most common being ringing/ghosting. This happens when part(s) of your printer vibrate as a result of the movement, and that vibration is transmitted to the nozzle and/or build plate, and appears in your print.

Input Shaping is not a new technique, but applying it to 3D printing is relatively new. I'm not going to talk you through the details of how to do it here - there is an excellent guide on the klipper site at https://www.klipper3d.org/Resonance_Compensation.html that I suggest you run through. Also do the acceleration selection section afterwards, that goes hand in hand with input shaper (it determines the maximum acceleration you can get away with before impacting your print quality).

Tip: if you go the route of the accelerometer, I suggest leaving the wires plugged into your Raspberry Pi and tucked away somewhere - if you do maintenance on your printer such as replacing belts, changing tensions etc then you're going to need to re-run this. Not having to flip your printer is a real positive.

Now go forth, make printer go "brrrr"....

[Back](README.md)