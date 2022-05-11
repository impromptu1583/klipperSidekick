# KlipperSidekick
Klipper config and macros for use with the Lulzbot sidekick

# WARNING
This is very much a work-in-progress config. Use at your own risk and please be safe.
Also, please review [Issue #1](https://github.com/mcmillanje/klipperSidekick/issues/1).

###I'm currently taking the approach of assuming the gantry is parked at zmax so make sure it's there before homing or you may damage your bed / toolhead!

## Firmware flashing
Follow the flashing instructions in [Klipper's Documentation](https://www.klipper3d.org/Installation.html)

Choose `Atmega AVR` as the architecture and `atmega2560` as the processor model on the menuconfig section.
![alt text](images/readme/01-menuconfig.png)

Follow the instructions closely and if you receive any timeout messages power the printer off and back on again then retry.

## configuration

TODO
z probe
toolhead
pid

## slicer config (CURALE or other)
Macros contains a START_PRINT and END_PRINT macro
Replace start gcode with:
```
START_PRINT BED_TEMP={material_bed_temperature_layer_0} EXTRUDER_TEMP={material_print_temperature_layer_0}
```
Replace end gcode with:
```
END_PRINT
```


## reference material
### hardware
Schematic: https://github.com/ultimachine/EinsyRetro/blob/1.0b/board/Project%20Outputs%20for%20EinsyRetro/Schematic%20Prints_EinsyRetro_1.0b.PDF
OHAI: https://ohai.lulzbot.com/group/taz-sidekick-289/