We're going to do this in two stages, first to get us into the right ballpark, and then to fine tune.

First up, open up SuperSlicer and use the flow calibration tool there. Using this you should be able to get within +/- 2% of the value you want.

Now, iteration time. This is tuning, get used to it. Two commonly used parts here are the Mobius 3 backplate for bearing fit, or the top of a Voron cube<sup>1</sup> for bearing fit. I've always used the cube, so that's what we're going to do. Drop the cube into your slicer, use the split object button (it's on the left edge of your screen) to just leave the top 6mm of the cube to save time, and get printing. I'd suggest printing 9 - one at what you think your perfect value is, and then 4 at +1% increments and 4 at -1% increments.

SuperSlicer has a useful feature to print all 9 variants at once. In the "3D view" tab, right-click the part; select "Add Settings"; and "Filament". Here you can enable an option to edit Extrusion Multiplier. If you copy and paste this part with this setting, you can create multiple instances of varying Extrusion Multiplier values. Note: this value is adjusted against the value defined in the Filament Settings (i.e. 96% of an EM of 0.85 would lead to an EM of 0.816).

This will get you pretty much bang on target, however, it's not foolproof. Do not ignore other signs in your test prints as you go along, you may find you need to tweak a % here and there. Believe what you see and understand it, then act, tuning printers is a logical puzzle at times.


1. https://github.com/VoronDesign/Voron-2/tree/Voron2.4/STLs/TEST_PRINTS


What to look out for:
* Does the bearing fit snugly without needing a lot of force?
If the bearing too big for the hole, try decreasing the extrusion multiplier

* At this point, don't worry about the first layer or the top finish - SuperSlicers has individual settings for those that we'll resolve later

* Does the bearing fit into all of the parts? Great, you're almost there!
Choose the extrusion multiplier that has the fewest defects in the side walls. If there are small holes, you may need to choose a slightly higher value.


[Back](README.md)
