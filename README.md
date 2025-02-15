# Klipper Configuration Files for a Modified Ender 3 V2 Printer

Welcome to the repository that houses meticulously crafted and then not so maticulously modified configuration files for a slightly modified Ender 3 V2 printer, with the stock extruder (although has been converted to direct drive), CR Touch, and a 4.2.2 silent board.  
just make sure to rename the 4.2.2 config to printer.cfg for it to work :p

## Overview

In this repository, you will find four essential configuration files: `printer.cfg`, `macros.cfg`, `Adaptive_Meshing.cfg`, `Line_Purge.cfg`. These files have been expertly tailored to optimize the performance of your modified Ender 3 V2 printer, enabling you to push the boundaries of print quality, accuracy, and speed.

## Features

- **Unleash Your Printer's Potential**: With our diligently crafted configuration files, you can tap into the full capabilities of your modified Ender 3 V2 printer. Experience a new level of performance that surpasses your expectations.
- **Fine-Tuned for Perfection**: We have invested significant effort in fine-tuning every aspect of the configuration, ensuring that each parameter is carefully optimized to deliver exceptional print results consistently.
- **Seamless Integration**: The provided `printer.cfg` file seamlessly integrates with the popular Mainsail interface, making it effortless for you to incorporate these configurations into your existing setup. Simply copy and paste the contents into your own `printer.cfg` file via Mainsail.
- **Simplified Customization**: Our configuration files are designed to be easily customizable, empowering you to tailor the settings to your specific requirements or modifications. Feel free to tweak and refine the configurations as needed to achieve the desired outcome.


## This config uses KAMP

- **What is KAMP?**

KAMP is a project that was created by kyleisah to simplify the usage of adaptive meshing on Klipper-based 3D printers. Adaptive meshing is the practice of using values from a gcode file to define a mesh's dimensions. This gives you the benefits of using a bed mesh, but only specifically where it is needed, without passing a bunch of variables around. KAMP was designed with simplicity in mind! 

Find out more about Kamp, https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging

## Getting Started

To embark on this journey of enhanced printing capabilities, follow these steps:

  1. Clone or download this repository to obtain the `printer.cfg`, `macros.cfg`, `Line_Purge.cfg`, and `Adaptive_Meshing.cfg` files.

  2. If you are using Mainsail, copy and paste the contents of the `printer.cfg` file into your existing `printer.cfg` file.
   add the following files to the same directory as the `printer.cfg` file:
   `macros.cfg`, `Line_Purge.cfg`, and `Adaptive_Meshing.cfg`

  3. You will also need to ensure the following is defined in moonraker.conf:
  
      [file_manager]
      enable_object_processing: True

  4. Replace the slicer's custom start and end g-code scripts with:

      Starting G-Code:
        START_PRINT BED_TEMP={material_bed_temperature_layer_0} EXTRUDER_TEMP={material_print_temperature_layer_0} 

      Ending G-Code:
        END_PRINT

  5. Enjoy the benefits of Klipper firmware and witness the remarkable improvements in your printing endeavors.

