So many squares...

If you have a bed that is totally flat then skip this part. For the rest of us mortals, read on.

You can set bed meshes with a variety of probe types, but the most consistent method I've found is doing it manually (mostly). For this I'm assuming we're on a V2.4 with an inductive probe. Bear in mind that it's entirely possible for your bed to be different shapes at different temperatures!

First up, run a bed mesh and save it to your printer. On my 300 I run a 7x7 as an example.

Next, you're going to make a slicer project that you'll want to save a copy of, because you won't want to do this dull task again. Create a 25mmx25mm square, the same height as your first layer (let's assume 0.2mm). Put it over the first probe location. Copy paste - second probe location. Copy paste - third....you get the idea. There's 49 to do. See you in a while.

Now load up that mesh you saved earlier and print your sliced grid of squares. Assess each one - a micrometer is best, vernier second, Mk1 eyeball if you have to. Remember that if you're too close to the bed and you squish up ridges then you're going to have a hard time measuring these. If in doubt, err on the side of "too high". Now you can use a spreadsheet I knocked up<sup>1</sup> to figure how what to tweak on your mesh, and repeat. If you're lucky, you'll have a perfect mesh in 3 iterations. If you're unlucky but thorough, it'll be 5 iterations. 



1. https://discord.com/channels/460117602945990666/461210576618651669/801559330214248468
