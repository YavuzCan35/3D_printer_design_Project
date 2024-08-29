# 3D_printer_design_Project
All aspects of mechanical, electrical and software components of the 3d printer is considered, combined and created by me. And project is currently completed.


Branches of project:

  1) Mechanical
  2) Electrical
  3) Software

Design considerations:

For mechanical design:
--------------------------
  Mechanical design considerations 1 : 
  
  Existing market designs are inspected. core xy, core z, delta and other 3d printer performances inspected with the data available online. Even though some designs like ender-3 have huge community supporting in case of a problem, the model specific base of the model is hard to modify if you want a build volume that you can increase or decrease in time.
  Delta printers are very fast and quite accurute. However technical maintanance and calibration are taking a lot of time due to the complex movement system. Furthermore the community of the delta printers are way smaller among other commercial models.
  Eventhough this will be a personal machine rather then professional, machine still must be precise enough to use for technical personal projects. Therefore we list the printers according to precision at this point. According to data, core xy printers have one of the most precise designs. In addition to this, they are quite scalable with the replacement of cheap frame.

  Mechanical design considerations 2 : 
  
  mechanical parts should be listed and modelled with a CAD software to so if they fit to design.
  Parts are as followed:
    Frame
    Gears
    Z mount
    Guides for movement
    Joints
    Motor mounts and couplings
    Power transmission elements

  For the frame, first choice to go for cheapest design. Best fit was cylindirical profiles. However the joints of such a frame required expensive joints and was not diverse enough to support possible design changes. Also they were not strong enough over certain distance.
  Therefore T slot aluminium profiles caught the eye. Even at smallest diameters like a 20x20 profile, theye were strong enough to support about a kilo in their weakest point without deforming. They were also accessible and relatively cheap for custom frame materials. Easily replacable if machine design will be changed to  bigger or smaller size.

  For gears, we should go for the simplest and common design. Therefore adoptation of existing commercial printer gears and gear mounts considered first. However this has limited the geometry and made it difficult to mount at a certain angle in a custom design. The price was also too high.
Therefore I designed a gear system myself. Using m4 and m3 screws as strut and idle plates as a floor and roof, using combination of toothed and toothless gear, I created my own gear design which is at least 60% cheaper then commercial designs but yet it can be easily assembled with standardized parts.

  Z mount have been done the last and to complete the design, local markets are used . Z mount design has been completely changed after completing the project due to low reliability. New design has not been uploaded. However briefly desribed, lead screw attached to a gantry plate right behingd it, which has been pushed form right and left by 2 T profiles. This increased and eased the stress falling to smallest movement element at z axis and increased the stability of the movement.

  Guides for movement are inspected and listed as linear rail and guide, V wheel gantry plates and some other options. Easiest maintanance and simplicity found in the gantry design. It was also the cheapest yet very steady.

  Joint options for T profiles was very cheap and endless. L connections or other triangle connectors are thought as support and 3 way joint was smooth and small enough to provide space for adding plates and gears to the right positions. It decreased the montage effort as well.

  Motor mounts and couplings are standardized enough to choose almost randomly. 1 coupling for lead screw motor neded and 2 screwd toothed gear for x and y motors was practical for a  belt driven machine.

  Power transmission elements are lead screw for the strength of Z axis against a heavy load and belt for x and y movements.


For electrical components:
---------------------------
  Electrical design considerations 1 :

  when existing designs inspected, it is obvious that it has at least these following items to function correctly:
    Motors, mainboard, power supply, motor drives, extruder, heated bed.
  
  Electrical design considerations 2 :

  Nema17 motors are most common motors on the commercial 3d printers, while nema23 motors are more common for cnc or milling machines. Nema23 motors are more powerful but more costly as well as their drivers and acustic profiles are way higher then nema17.
  
  When looked at the driver options like A4988 or tmc2226, there is a huge performance distance. Tmc motor driver futures microstepping and precision, which has huge benefits compared to a4988. Especially quiter work by the microstepping is a must for a indoor machine that will fwork for days for a single part. However the cost is fold by 15 times. A good comprimised found at one of the must common tmc models for 3d printers as TMC2209

  Mainboard sohuld have at least 4 driver slots as x,y,z and extruder. 30bit or higher boards are required for feasible speed and precision. Should allow enough current for the motors and other componnents. Therefore a design where simplicity and function is required drastacilly , SKR mini E3 V3 model with relatively new design for 3d printers looked promising as well as octoprint board. The main diffrence was skr board had built in tmc2209,eliminating the need of seperate test and assembly stage for drivers. therefore , it was practical, cheaper, simpler and new enough to fix some chronical 3d printing issues.

  Heated bed was the easiest of choices as there is nothing special about it.

  Power supply has been choosen after deciding all the system parts to calculate reqired power. For a 12 volt system required about 360 watts. However this has been later changed to 24volts due to efficieny issues.

  Extruder was completly problematic as there was not many options to buy whole extruder section. 3 main parts of extruder are hotend, feeder mount and motor.  The prepared kits were not presented with enough data on online ads. Therefore I decided to buy it piece by piece as I did to gears and which worked great. Therefore standart 24v hotend as well as 1A nema17 motor and a feeder mount has been bought at the cost of a extruder kit. After assembly and tests, it has been seen that the volume of the hotend was not enough for a high speed and quality extrusion. Therefore it has been replaced with a bigger hotend.
  
For software components:
------------------------
  Marlin and Klipper were 2 available most commmon options. However since Klipper required additional electrical computing unit which needs to be integrated , marlin was easier choice. The usage and quality diffrences were not big enough to go through with this additional cost.

  For a slicer that creates gcode for the printer, again there were many options. Ultimaker Cura has one of the best interfaces and customability for the slicing.





