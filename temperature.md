# Temperature tuning
Temperature tuning has to be one of the most written about aspects of printer tuning for beginners guides. The goal here is to find the highest temperature you can get away with before causing print issues.

The easiest way for this is using the inbuilt calibration tool in SuperSlicer1. Use the temperature calibration wizard and off you go. 

Three bits of advice on this:
1. Print at least 4 towers (adequately separated on the bed). You can confuse your results with layer times that are too short, resulting in insufficient time to cool the part between layers - in short, make the test representative of printing something real.
2. Don't make the towers too high! They can flex, a lot. I wouldn't go above 4 levels personally.
3. Play around with fan levels. Do a bit of reading and you'll get a feel for what people with a similar setup to you run for fan speeds. For ABS+ in a Voron you'll see values from 10% to 30% typically. Temperature and Fan are a balance, you may well have to iterate.
	* Looks melty? Temperature too high and/or fan too low
	* Layer separation? Temperature too low and/or fan too high

If you're not quite sure what temperature to go with (it's entirely common to see +/- 5C as an acceptable window) then pick the middle one for now - tuning retraction later may give you a better idea.

NOTE: A more complex method but one that is useful for in-depth tuning is doing a series of overhang towers (lots of STLs online). These typically look a bit like geometric flowers, with "petals" of increasingly severe overhangs, and you print several at different temperatures in order to give you that set of temperature/fan combinations.

# What to look out for
1. Do some features of the print look melty, squiggly, droopy? These features are probably not cooling down in time for the next layer to be added.
	* Check temperatures - is your filament temperature optimum?
	* Check layer time - small single parts need more time to cool before adding the next layer. Consider adding extra parts on the platter to increase layer time
	* Check fan % - listen to your printer and don't worry if you deviate (a little) from suggested profiles. All fans can be have different performance levels, but the effect of poor cooling is the same. 
		* NOTE: Changes to fan speed during a print may cause artefacts in your print (such as banding). Try to stick to a single fan speed if possible.
2. Are layers separating? The parts may be cooling down too much before the next layer is added.
	* Check temperatures - is your filament not hot enough? is your bed hot enough for those first few layers?
	* Check fan % - are you over cooling the material? Can the part fan be turned down without detail suffering?
	* Monitor enclosure temperature - are you printing in an enclosure? Is the ambient temperature / too low?

# A note on warping
There may be many reasons for why your print is warping. Tune separately to the temperature values discussed here.
* Are sections of the part cooling quicker than others? Check for draughts; check enclosure; check bed temperature
* Is the z-height configured properly?  More smush required?
* Is the bed surface contributing? Consider cleaning the bed or using an adhesive suitable for your printing material

[Back](README.md)

Links:
https://github.com/supermerill/SuperSlicer
