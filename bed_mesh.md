So many squares...

If you have a bed that is totally flat then skip this part. For the rest of us mortals, read on.

You can set bed meshes with a variety of probe types, but the most consistent method I've found is doing it manually (mostly). For this I'm assuming we're on a V2.4 with an inductive probe. Bear in mind that it's entirely possible for your bed to be different shapes at different temperatures!

First up, run a bed mesh and save it to your printer. On my 300 I run a 7x7 as an example.

Next, you're going to make a slicer project that you'll want to save a copy of, because you won't want to do this dull task again. Create a 25mmx25mm square, the same height as your first layer (let's assume 0.2mm). Put it over the first probe location. Copy paste - second probe location. Copy paste - third....you get the idea. There's 49 to do. See you in a while.

Alternatively, use this OpenSCAD script to generate the test squares for you. You'll need to set `probe_count`, `mesh_min`, and `mesh_max` variables based on the settings your printer uses for generating a bed mesh. If you're using klipper, these are under the [bed_mesh] section in your printer.cfg. See https://www.klipper3d.org/Bed_Mesh.html for more info.

    /* [MESH] */
    // The number of spots probed along the X and Y axes. A 3x3 mesh probes a total of 9 points, 5x5 a total of 25, etc.
    probe_count_x=7; // [3,5,7,9]
    probe_count_y=7; // [3,5,7,9]

    // The minimum X and Y coordinates of the bed mesh. Typically this would be the probe point in the very front-left corner of the bed.
    mesh_min_x=30;
    mesh_min_y=30;

    // The maximum X and Y coordinates of the bed mesh. Typically this would be the probe point in the very back-right corner of the bed.
    mesh_max_x=220;
    mesh_max_y=220;

    /* [PRINT SETTINGS] */
    // Should match the first layer height configured in your slicer.
    first_layer_height=0.20; // [0.1:0.01:2]

    /* [TEST SQUARE] */
    // Decrease if there are no gaps between your generated squares. The default of 25 should be fine for most bed sizes.
    test_square_size=25; // [1:35]

    for (x_coord = [0:probe_count_x-1]) {
        for (y_coord = [0:probe_count_y-1]) {
            translate([mesh_min_x + x_coord * ((mesh_max_x-mesh_min_x)/(probe_count_x-1)), 
                    mesh_min_y + y_coord * ((mesh_max_y-mesh_min_y)/(probe_count_y-1)),  
                    0])
                cube([test_square_size,test_square_size,first_layer_height],center=true);
        }   
    }

Now load up that mesh you saved earlier and print your sliced grid of squares. Assess each one - a micrometer is best, vernier second, Mk1 eyeball if you have to. Remember that if you're too close to the bed and you squish up ridges then you're going to have a hard time measuring these. If in doubt, err on the side of "too high". Now you can use a spreadsheet I knocked up<sup>1</sup> to figure how what to tweak on your mesh, and repeat. If you're lucky, you'll have a perfect mesh in 3 iterations. If you're unlucky but thorough, it'll be 5 iterations. 



1. https://discord.com/channels/460117602945990666/461210576618651669/801559330214248468

[Back](README.md)
