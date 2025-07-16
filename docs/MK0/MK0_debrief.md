# MK0 - Basic Prototype

<img src="./images/full_printer3.jpg" alt="pic" width="600"/>

## Background

It's not pretty... but it works

The primary constraint with this initial prototype is one many people run into when building their first 3d printer. That is, that I didn't have a 3d printer. Since I couldn't easily prototype or manufacture custom parts I limitted myself to using only parts I could make using basic tools. These tools included a jig-saw, a power drill, A soldering iron and a variety of hand tools. 

I opted to start with a relitively large build area. My initial plan was to have a full 300mm cubic build space though unfortunately for this initial prototype I ended up having to limit that to 175mm x 175mm x 250mm (more on that later). This may have been for the best as bed leveling has proven challenging on this initial build.

While it's my intention to create my own printhead for this project I initially used a direct drive head from an Anycubic Kobra 2. I selected this for it's low cost and the fact that it was complete and self contained. A word of caution is that Anycubic does not open source their hardware or software so I did have to do some reverse engineering to get it working. I will not be publishing the details of that reverse engineering to avoid posting any copywritten IP.

The printer is based on the REPRAP 1.4 control board using an Arduino MEGA board. It operates using Marlin firmware.

## Build Overview

The main frame is built using a combination of aluminum extrusion and composite wood panelling that has been cut to sizes/shape and drilled as required. It is held together with a combination of metric hardware and zip-ties.

As discussed prior I am using an Anycubic printhead which moves in X on a belt driven carriage. The X-axis then moves verticly (Z) on a pair of lead screws.

The bed is a pane of glass which slides in the Y direction (Forward and Back) on a belt drive. This glass pane is supported by 4 bolts which can be adjusted to level the print bed.

Currently the electrical components (REPRAP board and power supply) are stored on the table beside the printer.

## Configurations

Full config details can be found in the Marlin configuration document here:  
[Configuration.h](../../software\Marlin-2.1.2.5\Marlin\Configuration.h)  

All stepper motors are set up to use 1/16 microstepping.

As mentioned above I have restricted the printer to use a 175x175x250mm build space. At time of writing I have not yet tested larger prints but will be doing so shortly.

In my initial testing I had the Z axis bind when using too high of a feedrate. For this reason I have significantly limitted the speed of the printer. I have not tested the limits for these metrics as yet but will begin increasing them slowly as I begin building the parts for MK1.  




## Lessons
While perfection was never the goal here this project was not without it's problems. Below I would like to detail some of the main issues I encountered building this prototype and discuss the lessons learned from them. 

### Bed Size and Verticle Rods
As mentioned earlier I had to reduce the bed size from my projected 300mm cubed to 175x175. This was due to the geometry of the x and y axis. 

For the X-axis I opted to have the verticle rods sit inside the frame. This choice was made to simplify the brackets used to hold these rods. Additionally since I was using composite panels I ended up having to make the X carriage and brackets larger than expected which blocks some of the X travel.

The Y-axis has similar issues with the size of it's brackets but also could be corrected by placing the bearings closer together so that the bed could hang over these brackets further.

This is also the reason I am using a plain glass panel as a print surface. I purchased a removable build plate which I will be using for future iterations but it does not fit on the current build.

### Z-Endstop Relocation
In my initial design I had the Z-Endstop at the top of the axis. When testing I found it was very difficult to get a consisting starting position on prints. To mitigate this I moved the endstop to the bottom.

The major difference here is that when the endstop is at the top you can configure the starting position via software. Now the endstop would need to be physically moved to adjust the height from the build plate. 

This may be less of an issue in future builds where the frame and axis have less slop. In all likelyhood I will eventually switch to a bed probe of some kind so I am not to concerned about this going forward. 

### Bed Leveling Issues
My bed leveling mechanism consists of 2 panels. The lower panel holds the bearing and has a bolt in each corner. These four bolts are placed from below facing up with a nut placed loosely on them. tightening or loosening the nut adjusts how much of the bolt stands above the plate while the remainder of the bolt hangs below.

The upper panel holds the glass buildplate. Glued to the bottom of the upper plate are 4 spacers which sit overtop of the bolts.  

This system works but can be frustrating to use for the following reasons. 
- There is quite a bit of slop between the two plates
- 4 Adjustment points are being used when only 3 are required
- Bolt must be held while nut is turned
- Nuts/Bolts can be very hard to reach

### Wood Panelling is not Nice
Because I am the way I am, I went to the hardware store and bought the cheapest "wood" I could find to create the brackets. This came in the form of a composite paneling which appears to be some kind of compacted cardboard product... 

While functional it is deeply unpleasant to work with. It flakes away in layers when being drilled or cut and produces huge amounts of dust and shavings. if I was doing this again I would definitely spend a few extra dollars for a better material.

### Hotend Sag
Because I used a direct drive extruder the hotend is fairly heavy. This combined with the makeshift X carriage causes the printhead to sag. This means the hotend is not perpendicular to the build plate. 

The problem is not significant enough to cause prints to fail but definitely influences the quality. For the next iteration I will be creating a new X carriage and printhead bracket so this issue will be corrected at that point.

## Next Steps

- Replace The Panelling and Zip Ties
- Straighten Belt Runs and Add Tensioners
- Create Room for Full Sized Bed
- Create Better Bed Leveling System
- Remodel Print Head Carriage
- UART for Motor Controllers
- Increase Print Speeds
- Add Electrical Board and Fix Wire Routing