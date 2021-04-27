I'll keep this short as temperature tuning has to be one of the most written about aspects of printer tuning for beginners guides. The goal here is to find the highest temperature you can get away with before causing print issues.

The easiest way for this is using the inbuilt calibration tool in SuperSlicer1. Use the temperature calibration wizard and off you go. Three bits of advice on this:
	- Print at least 4 towers. You can confuse your results with layer times that are too short, resulting in insufficient time to cool the part between layers - in short, make the test representative of printing something real.
	- Don't make the towers too high! They can flex, a lot. I wouldn't go above 4 levels personally.
	- Play around with fan levels. Do a bit of reading and you'll get a feel for what people with a similar setup to you run for fan speeds. For ABS+ in a Voron you'll see values from 10% to 30% typically. Temperature and Fan are a balance, you may well have to iterate.
		○ Looks melty? Temperature too high and/or fan too low
		○ Layer separation? Temperature too low and/or fan too high

If you're not quite sure what temperature to go with (it's entirely common to see +/- 5C as an acceptable window) then pick the middle one for now - tuning retraction later may give you a better idea.

NOTE: A more complex method but one that is useful for in-depth tuning is doing a series of overhang towers (lots of STLs online). These typically look a bit like geometric flowers, with "petals" of increasingly severe overhangs, and you print several at different temperatures in order to give you that set of temperature/fan combinations.
