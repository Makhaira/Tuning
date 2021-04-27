Top Flow is adjusting the Flow/Extrusion Multiplier for just the topmost layer in order to improve surface finish. Not all slicers have this, but SuperSlicer does.

Ok, the thinking behind my approach to this is to eliminate the effect of infill/perimeter overlap whilst tuning the top flow. To do that we need a big enough surface area that infill/perimeter overlap is negligible in influencing the top surface finish. I went for a 50mm x 50mm cuboid, just a few mm high. Is that too big? Maybe, but it does the job. Feel free to experiment with smaller sizes.

Height-wise, I just slice it such that the top section is representative of a "real" print. So if I normally have 5 top layers on top of 40% gyroid, I'm going to make sure I get at least one layer of gyroid infill printed, and then the 5 top layers.

Most people find starting around 85% puts you in the right area, but don't be surprised to end up anywhere from low 80's to low 90's.

NOTE: Now an entirely optional thing you can do to further improve your top surface is to also play around with your extrusion width. For a 0.4mm nozzle, try setting your top layer extrusion width to around 0.32. This results in a greater number of passes with the nozzle, which also overlaps the previous layer to a greater degree than normal. The result? Some silky smooth top layers with a fraction of the time impact you get from ironing.
