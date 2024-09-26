# NightTurtle: Integrated Dual Spool Filament Switching System

NightTurtle is an enclosure that integrates multiple projects' technologies into a dual-spool filament switching system.

![1](./Images/nightturtle-render.png)

## Summary

The goal of the NightTurtle enclosure is to create a simple, universal filament switching solution that accommodates two primary usage styles: standalone units with integrated rewinding filament spool holders, or backpack-style units mountable to a printer, fed from separate spool rollers. A secondary objective was to design a mostly self-contained setup requiring only a 24V power supply and either a USB or CAN connection.

To achieve this, NightTurtle integrates the following projects:

- Hartk's [Dual Nightwatch](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch): a compact dual Bowden extruder based on the Voron Nightwatch
- Hartk's [Bowden Y-Splitter](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch/STLs/Bowden_Y)
- [Filamentalist Rewinder](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Filamentalist_Rewinder) from the Enraged Rabbit Community
- Fysetc [ERB 2.0 MCU](https://github.com/FYSETC/FYSETC-ERB/tree/main/V2.0)
- Annex Engineering's [Belay](https://github.com/Annex-Engineering/Belay) Extruder Sync Sensor

Alternatively, the [ERCF Filament Stress Sensor](https://www.printables.com/refresh?redirectUrl=%2Fmodel%2F803180-voron-ercf-filament-stress-sensor) is also compatible.

## Printing

Print the following components:

- Base plate
- Filament mount
- Skirt files (all)

Additionally, select and print the top plate suitable for your specific use case.

Note: The knobs are only necessary when using the backpack top panel.

### Print Settings

All parts have been pre-oriented for support-free printing or include integrated supports. Print using the recommended Voron settings:

- Layer height: 0.2mm.
- Extrusion width: 0.4mm, forced.
- Infill percentage: 40%
- Infill type: grid, gyroid, honeycomb, triangle, or cubic.
- Wall count: 4
- Solid top/bottom layers: 5
- Supports: **NONE**

To correctly print the honeycomb pattern, split the skirt STL into separate objects in your Slicer and set the type to 'Modifier' for the inlay/mesh modifier part. Configure the modifier settings as follows for optimal print results:

![2](./Images/prusa-modifier-settings.png)

## Assembly

Please refer to the [Bill of Materials](./BOM.md) for a list of parts needed for the enclosure. Additionally, check the projects listed in the summary for specific parts requirements.

### Step-by-Step Assembly

1. Insert 16 Voron-spec heatset inserts into skirt mounting points.
2. Install 4 heatset inserts into the top of the base plate pillars.
3. Install 4 heatset inserts into Dual Nightwatch mounting holes.
4. Install 2 heatset inserts into the filament splitter mount.
5. Install 3 heatset inserts into MCU mounting posts.
6. Install 4 heatset inserts into the top panel:
   1. Either into the 4 mounting points for Filamentalist Rewinders.
   2. Or into the 4 knobs for the backpack top panel.
7. Remove the integrated support from the XT30 2+2 connector opening in the base plate.
8. Install the ERB 2.0 MCU into the base plate.
9. Install the blank skirt on the side with the MCU.
10. Install the 40mm axial fan (10-20mm depth verified) into the fan skirt and mount it to the opposite side of the MCU.
11. Install the Dual Nightwatch onto the base plate.
12. Install two ECAS connectors into the skirt with filament inlets; be mindful of force to avoid damaging the honeycomb pattern.
13. Install the filament inlet skirt in the base plate; feed in PTFE tube from outside until securely seated in the Dual Nightwatch.
14. Install the filament splitter mount; route the Belay tension sensor cable/connector outside through the mount.
15. Assemble the filament splitter; connect it to the Dual Nightwatch using two PTFE tube lengths. Adjust tube length for flush mounting.
16. Attach the skirt with the filament outlet to the base plate.
17. Install 10x3 countersunk magnets into the base plate and top panel. Monitor screw length to avoid damaging prints.
    Note: For 2.6mm magnets, use M3 washers as shims.
18. If using spool holders, mount them with 4 FHCS screws from the top panel's bottom and 4 SHCS screws into heatset inserts.
19. Finally, wire up the XT30 2+2 connector and test everything before installing it into the base plate.

## Images

Soon(tm)

## License

This work is licensed under the GNU General Public License v3.0, for more details check the [LICENSE](./LICENSE).
