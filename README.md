Easy DXF stack generator
This project is a custom tool that enhances the DXF2Gcode project with features optimized for single-layer 3D printing and specific G-code modifications. It adapts DXF files for additive manufacturing, especially Melt Electro Writing, includes height and extrusion calculations, and provides tools for organizing G-code blocks.

Features
DXF to G-code Conversion: Converts DXF files to G-code for single-layer 3D printing.
Extrusion and Height Calculations: Automatically calculates extrusion rates and height values based on specified factors.
G-code Inversion: Reverses G-code vectors and order to make the machine move from the end position back to the start.
Block Management: Ensures correct G-code block structures, preventing nested and overlapping blocks.
Configuration Management: Automatically copies custom configuration files to the user's .config directory.
Installation
Clone the Repository:

git clone https://github.com/Anercomp/Easy-DXF-stack-generator.git

This build already comes with dxf2gcode. Notepad++ is not needed but recommended, as well as NCnetic. Every tool and ressource can be checked with the top right button. This will take care of Notepad++ recognition, NCnetic installation and a gcode block UDL. 

Usage
G-code Editing:

Open your G-code in the provided editor.
Use the "Insert Extrusion Block" feature to add custom extrusion blocks.
The program ensures each block is well-structured, with proper start and stop markers and no nesting issues.

Adjusting Extrusion and Height:
The parameters after a block start override the value specified in the up-down boxes.
Modify the inserted extrusion factor or block height using the up-down boxes, automatically applying height increments based on the block’s length.

G-code Visualization:
The program displays G-code paths visually in a PictureBox, allowing zoom and pan adjustments.
Arrow markers with adjustable size show the direction of each G-code segment with the last path being marked with a yellow arrow.

Invert G-code Path:
Reverse the G-code path and vectors to have the machine retrace its path in reverse order.

Configuration
The program uses postpro_config.cfg and config.cfg files for settings. These should be located in your .config\dxf2gcode directory after installation.

Troubleshooting
Configuration File Location: Verify that the configuration files are correctly copied to the user's .config directory.

This project makes use of dxf2gcode from https://sourceforge.net/projects/dxf2gcode/. Big thanks to Christi_ko for fixing bugs relevant for this project and of course dwrobel, jp1357, neveruml, rli, treki, andyz, innerbushman, poofjunior, propcoder, sanzamoyski and seb_kuzminsky for developing dxf2gcode. 
