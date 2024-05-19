# PixieForge
An ultra-portable, foldable 3D Printer.  

<img src="/pictures/render_front.png" width="50%">  

## What is it?
The PixieForge is a small 3D printer that folds up when not in use, making it small enough to fit inside a filament box.  
This project started as a simple extension of [eponra's flatpack 3D printer](https://github.com/eponra/flatpack/), but quickly turned into a complete redesign with a focus on ease of use and reliability.

The foldable design makes it suitable for anyone who either doesn't have the space for a printer or wants to use it on the move.  

<img src="/pictures/render_folded.png" width="50%">

## Technical specifications
- Print volume: 120x120x120mm
- Machine size folded: 205x206x79mm
- Max. Bed temperature: 120°C (using a Voron0 bed)
- Max. Hotend temperature: 300°C (using a TriangleLabs CHC mini)
- Extruder system: Bowden (using a modified Sherpa Micro)
- Power consumption: not yet measured. Approx 120W peak and much less during operation
- Power input: 24V, 5.5mm barrel plug (150W power supply recommended, but could run on battery)
- Bed levelling: BLTouch/Automatic
- Controller: BTT SKR pico + Raspberry Pi Zero 2W (running on Klipper)

## Design choices
**Ease of use and accessibility**  
Wherever possible, the PixieForge uses parts that are compatible with other open source projects, making sourcing much easier.  
Most of the printed parts don't need supports and the build process is fairly straightforward (although a little finicky).  
Also, the price for a complete machine should be under 350$.

**Reliability**  
The PixieForge is designed to make as few compromises as possible (obviously some had to be made).  
It is fully capable of printing technical materials, uses automatic bed leveling, runs Klipper and so on...  
As the hotend assembly is modular, it can be easily adapted to work with other hotends.  
It currently uses the TriangleLabs CHC Mini, which has a quick-change heatbreak/nozzle assembly (using M6 nozzles).

**Compromises**  
This printer uses fixed-bed cantilever kinematics (i.e. the bed is fixed and the whole Z-tower moves along the X-axis).  
These kinematics aren't the best choice in terms of rigidity, but they do allow the printer to fold up and free up space under the bed.  
For such a small printer this won't be a problem, just don't expect to break any speed records.  

Currently there is no display on the machine.  
It is fully controlled via WiFi and the end device of your choice. Hopefully this will change in a future release.  

## Next Steps  
- Finishing the Github Repo, finalizing the BOM, etc.

**short-term**
- Stress-testing the printer and using it.
- Evaluating speed and power draw.
- Creating a building-manual.
- Creating nicer looking CAD files for aftermarket parts.  
- Adding all fasteners to the CAD assembly.  

**long-term**
- Redesigning the electronics-bay and adding the option for a display.
- Adding support for more hotends.
- Further reducing cost.

## Contributions
I'd like to thank everyone in the flatpack group for their support during the development of this project! Especially eponra for creating an awesome 3D printer.
