# MK0 - Basic Prototype

<img src="./images/full_printer3.jpg" alt="pic" width="600"/>

## Background

It's not pretty... but it works

The primary constraint with this initial prototype is one many people run into when building their first 3d printer. That is, that I didn't have a 3d printer to start with. Since I couldn't easily prototype or manufacture parts custom parts I limitted myself to building this initial prototype using only parts I could work with using only basic tools. These included a jig-saw, a power drill, A soldering iron and a variety of hand tools. 

I opted to start with a relitively large build area. My initial plan was to have a full 300mm cubic build space though unfortunately for this initial prototype I ended up having to limit that to 175mm x 175mm x 250mm (more on that later). This may have been for the best as bed leveling has proven challenging on this initial build.

While it's my intention to create my own printhead for this project I opted to initially use a direct drive Anycubic Kobra 2 printhead. I selected this for it's low cost and the fact that it was complete and self contained. A word of caution is that Anycubic does not open source their hardware or software so I did have to do some reverse engineering to get it working. I will not be publishing the details of that reverse engineering to avoid posting any copywritten IP.

The printer is based on the REPRAP 1.4 control board using an Arduino MEGA board. It operates using Marlin firmware.

## Build Overview

The main frame is built using a combination of aluminum extrusion and composite wood panelling that has been cut to sizes/shape and drilled as required. It is held together with a combination of metric hardware and zip-ties.

## Configurations

Full config details can be found in the Marlin configuration document here:  
[Configuration.h](../../software\Marlin-2.1.2.5\Marlin\Configuration.h)  

All stepper motors are set up to use 1/16 microstepping.

As mentioned above I have restricted the printer to use a 175x175x250mm build space. At time of writing I have not yet tested larger prints but will be doing so shortly.

In my initial testing I had the Z axis bind when using too high of a feedrate. For this reason I have significantly limitted the speed of the printer. I have not tested the limits for these metrics as yet but will begin increasing them slowly as I begin building the parts for MK1.  

## Lessons

### Bed Size and Verticle Rods

### Z-Endstop Relocation

### Bed Leveling Issues

### Wood Panelling is not Nice

### Hotend Sag

## Next Steps

### Replace The Panelling and Zip Ties

### Straighten Belt Runs and Add Tensioners

### Create Room for Full Sized Bed

### Create Better Bed Leveling System

### Remodel Print Head Carriage

### Increase Print Speeds