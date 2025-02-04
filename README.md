# NightOwl: Integrated Dual Spool Filament Switching System

NightOwl is an enclosure that integrates multiple projects' technologies into a dual-spool filament switching system.

![1](./Images/nightowl-render.png)

## Summary

The goal of the NightOwl enclosure is to create a simple, universal filament switching solution that accommodates two primary usage styles: standalone units with integrated rewinding filament spool holders, or backpack-style units mountable to a printer, fed from separate spool rollers. A secondary objective was to design a mostly self-contained setup requiring only a 24V power supply and either a USB or CAN connection.

To achieve this, NightOwl integrates the following projects:

- Hartk's [Dual Nightwatch](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch): a compact dual Bowden extruder based on the Voron Nightwatch
- Hartk's [Bowden Y-Splitter](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch/STLs/Bowden_Y)
- [Filamentalist Rewinder - 80mm Axle](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Filamentalist_Rewinder) from the Enraged Rabbit Community
- Fysetc [ERB 2.0 MCU](https://github.com/FYSETC/FYSETC-ERB/tree/main/V2.0)
- ArmoredTurtle's [TurtleNeck](https://github.com/ArmoredTurtle/TurtleNeck) syncing toolhead buffer

Besides these parts you'll also want an extruder that has both a toolhead and an entry sensor. Some options for this are:

- [Clockwork 2](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Toolhead_Modifications/Stls)
- [WristWatch G2](https://github.com/bythorsthunder/Voron_Mods/tree/main/Wristwatch_G2_Dual_Filament_Sensor/STLs)

## Printing

Print the following components for the NightOwl.

- 1x Base plate
- 3x Blank Corner
- 1x Connector Corner
- 1x Connector Insert for your choice of connectors
- 1x Top Plate of choice (80mm Filamentalist or Backpack )
- 1x Y-Splitter Mount
- 4x Skirts
  - Front
  - Back
  - Left
  - Right
- 4x Feet (if using the Filamentalist top)
- 4x Knobs (if using the Backpack top)

## Other parts to print

- [Dual Nightwatch](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch/STLs/Dual_Nightwatch)
  - Use the 2-part guidler, it has proven more reliable than the single piece guidler
  - Prefer the mid body with collets for improved reliability
- [Y-Splitter](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch/STLs/Bowden_Y)
  - Only print the mid body and the rear cover
- [Filamentalist](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Filamentalist_Rewinder)
  - Please use the files provided [in this repository](./STL/Filamentalist/), they are adjusted to fit slightly wider spools.
    Files in the directory are following the naming conventions in the manual and will yield the required two rewinders.

### Print Settings

All parts have been pre-oriented for support-free printing or include integrated supports. Print using the recommended Voron settings:

- Layer height: 0.2mm.
- Extrusion width: 0.4mm, forced.
- Infill percentage: 40%
- Infill type: grid, gyroid, honeycomb, triangle, or cubic.
- Wall count: 4
- Solid top/bottom layers: 5
- Supports: **NONE**

The skirts have been provided as 3MF files with the correct settings applied for PrusaSlicer. However, if your slicer does not support importing these settings, open the 3MF in geometry-only mode and change the type of the inlay/mesh modifier part to 'Modifier'. Then, configure the modifier settings as follows for optimal print results:

![2](./Images/prusa-modifier-settings.png)

## Assembly

### Bill of Materials

Please refer to the [Bill of Materials](./BOM.md) for a list of parts needed for the enclosure. Additionally, check the projects listed in the summary for specific parts requirements.

### Assembly Instructions

The [Assembly Manual](./Manual/Assembly%20Manual.pdf) provides detailed, step-by-step instructions for assembling your NightOwl.

## Images

Soon(tm)

## Acknowledgements

The NightOwl project builds upon open-source innovations, drawing inspiration from the [BoxTurtle](https://github.com/ArmoredTurtle) project. While influenced by BoxTurtle's design philosophy, NightOwl distinguishes itself through deliberate design choices: minimal footprint, dual-channel limitation and leveraging off-the-shelf components.

## Changelog

- 2025-02-03 NightOwl 1.0 (Flamboyant Flamingo)
  - Update front skirt (removed ECAS couplers)
- 2025-01-07 NightOwl RC.2 (Ethereal Elk)
  - Changed corners and top plates to use standard 6x3mm magnets
- 2024-11-29 NightOwl RC.1 (Derpy Dingo)
  - Included customized Filamentalist Parts
    - Parameters adjusted to allow for up to 74mm wide spools (instead of 68mm) with identical hardware.
  - Updated top panel to match the Filamentalist rewinders
  - Correctly tagged connector inserts with accent color
  - Fixed undersized hole in bottom panel
  - Fixed various quantities in the BOM
  - Made dual Micro-Fit connectors the recommended option
  - TurtleNeck is the default recommended filament tension sensor
- 2024-10-18 NightOwl Beta.1 (Crafty Crow)
  - Simplified the corners
    - Switch to an insert base approach for connectors
    - Single blank corner with universal mounting holes
    - Moved all connectors to the "back"
  - Added markers to the bottom plate where the various corners go
  - Added hints to parts printing for Nightwatch and Y-Splitter
  - Updated Bill of Materials with more sourcing links
- 2024-10-07 NightOwl Alpha.2 (Brawny Beaver)
  - Bill of Materials added
  - Increased height of enclosure by 4mm
  - Revised MCU mount to add support for BTT MMB 1.0 MCU
  - Added the option to use compressor feet
  - Updated to the latest dual nightwatch release (v16)
  - Moved MCU connectors to the back by default
    - Optional corners are provided to use XT30 2+2 or MicroFit 3.0 for the MCU connection
    - Optional corners to keep the MCU connection in the front corner (for backpack style use)
- 2024-09-25 NightOwl Alpha.1 (Ambitious Alpaca)

## License

This work is licensed under the GNU General Public License v3.0, for more details check the [LICENSE](./LICENSE).
