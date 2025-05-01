# PRINT ALL THE THINGS!

## A Quick Note

This repo will probably be pretty sparse for a while. Im still in the early stages of this project but I wanted to create a place to begin accumulating models, design documentation and parts research. Ill keep this readme updated as things develop.

## Design Considerations

My intention is to build a Cartesian printer similar to a Prusa i3 or Ender-3. Y motion will be applied to the print plate while the hot-end will move in the X and Z directions. It's my feeling that this will provide the most straightforward framework to develop a working printer which I can iterate and improve upon over time.

I am tentitively planning a print surface of 300 x 300 x 300 mm.

## Parts

My initial approach to part selection is to minimize cost where ever reasonable. At this point my goal is to build a functional printer without a strong focus on print speed or quality (yet). Through doing so I hope to develop my own skills and identify any knowledge gaps or incorrect assumptions I have.  

Once I have created a prototype device and rectified any design issues that become clear during that process I will begin iterating on the device and replacing those lower cost parts with higher end equipment where necessary to improve overall quality.  

## Modelling

The model will be broken into 3 primary sections, one for each axis. The Y-axis assembly will include the print plate while the X-axis will include the hotend and extruder. Each of these main assemblies will be further divided into sub assemblies to isolate different segments such as motor drives, frame segments, ect. 

### Y-Axis

I will be tackling the Y-Axis first as it includes both the print surface and the devices base.

#### Parts to be Modeled

- [x] Extrusions
- [x] Linear Slider
- [ ] Linear Rail
- [ ] Print Surface and Plate
- [ ] Bracket for Plate
- [ ] Assorted Connectors
- [ ] Motor
- [ ] Motor Bracket
- [ ] Pulleys
- [ ] Timing Belt

### X-Axis

### Z-Axis