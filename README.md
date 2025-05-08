# PRINT ALL THE THINGS!

<img src="./images/full_build.PNG" alt="drawing" width="500"/>

## A Quick Note

This project is still in the design phase and as yet remains unproven. 

## Design Considerations

My intention is to build a Cartesian printer similar to a Prusa i3 or Ender-3. Y motion will be applied to the print plate while the hot-end will move in the X and Z directions. It's my feeling that this will provide the most straightforward framework to develop a working printer which I can iterate and improve upon over time.

- Print Area: ~300 x 300 x 300 mm 
- Total Size:  400 x 540 x 540 mm
- Frame Material: 2020 Aluminium Extrusion (T-Slot)

- 8mm Linear Rods and Bearings 
     - 2 per axis

- Actuation:
     - X and Y Axis: 6mm Belt
     - Z-Axis: Dual Lead Screws

- V_CPU: 3.3V
- V_IN : 24V

- Stepper Motors (Nema 17) Total: 5
     - Y-Axis: 1
     - X-Axis: 1
     - Z-Axis: 2
     - Extruder: 1

## Electrical

| Part               | Part Detail   | Number | Voltage      | Power          | Comment                             |
|--------------------|---------------|--------|--------------|----------------|-------------------------------------|
|Stepper             |Nema 17        | 5      |  12V - 24V   | 20.4W - 40.8W  |                                     |
|Motor Controllers   |?              | 4      |              |                | Z-Axis can share controller, May be included in control board         |
|Hot End             |? E3D V6       | 1      |              |                |                                     |
|Control Board       |? BigTree SKR  | 1      |              |                | I'm interested in making my own but will wait until things are running|
|Limit Switches      |Leaf Switches  | 3      |              |                |                                     |
|Heated Bed          |?              | 1      |              |                | Will probably leave off initial build and upgrade later |
|PSU                 |?              | 1      | 24V          |                |                                     |
|Step Down Converter |?              | 1      | 24V -> 3.3V  |                | May be included in controller       |
|Fans                |               | 1+     | 12-24V       |                |                                     |  

## Modelling

The model will be broken into 3 primary sections, one for each axis. The Y-axis assembly will include the print plate while the X-axis will include the hotend and extruder. Each of these main assemblies will be further divided into sub assemblies to isolate different segments such as motor drives, frame segments, ect. 

All models will be created using FreeCAD 1.0. FreeCAD can be downloaded at the following link to access or modify the files:

https://www.freecad.org/

### Models

#### Full Frame

<img src="./images/full_frame_05_06.PNG" alt="drawing" width="500"/>

#### Y-Axis

<img src="./images/Y-Axis_05_07.PNG" alt="drawing" width="500"/>

#### X-Axis

#### Z-Axis

## Parts

My initial approach to part selection is to minimize cost wherever reasonable. At this point my goal is to build a functional printer without a strong focus on print speed or quality (yet). Through doing so I hope to develop my own skills and identify any knowledge gaps or incorrect assumptions I have.  

Once I have created a prototype device and rectified any design issues that become clear during that process I will begin iterating on the device and replacing those lower cost parts with higher end equipment where necessary to improve overall quality.

### Custom Parts

I've encountered a few places where the most cost effective, straightforward or easily available solution is to design a custom part. Unfortunately, I dont currently have access to a 3d printer. My hope is that I can  use woodblocks, zipties and prayers to hold the design together well enough to print rough copies of these parts and refine things from there. If that proves impossible I will reach out to a printing service or local makerspace to create these parts.

#### Offset Rod End Caps

#### Timing Idler Mount

### Parts to be Modeled

#### General

- [x] Extrusions
- [x] Linear Bearing
- [x] Linear Rails
- [x] Motor
- [x] Motor Bracket
- [x] Timing Idlers
- [x] Belt Clamps

#### Y-Axis

- [x] Print Surface Plate
- [x] Spacer/Crossbeams for plate (Currently being interfered with by rails end caps, needs tp be higher)

#### X-Axis

- [ ] Hot End
- [ ] Extruder
- [ ] Hot End and Extruder Brackets

#### Z-Axis

- [ ] Filament Holder
- [ ] XZ-Axis Connector Brackets

