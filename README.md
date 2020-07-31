Cmod A7-15T Out of Box Demo 
====================

Description
-----------

This project demonstrates how to use the Cmod A7-15T's Artix 7 FPGA's Microblaze processor with the SRAM, LED's, RGB LED's, Pushbuttons and the USB UART bridge. Vivado is used to build the demo's hardware platform, and Vitis is used to program the bitstream onto the board and to build and deploy a C application. 

To use this demo, the Cmod A7-15T must be connected to a computer over MicroUSB, which must be running a serial terminal. For more information on how to set up and use a serial terminal, such as Tera Term or PuTTY, refer to [this tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).

Whenever the demo is started from Vivado SDK, the board will go through a memory test and will print out the result to the serial terminal. Whenever one of the buttons is pressed, the line “Button Pressed” is sent. Every time BTN1 is pressed, the LED state changes. The user LEDs create a 2 bit binary counter that increments every time the button is pressed.  The RGB LED smoothly transitions between colors.

Requirements
------------
* **Cmod A7-15T**: To purchase a Cmod A7-15T, see the [Digilent Store](https://store.digilentinc.com/cmod-a7-breadboardable-artix-7-fpga-module/).
* **Vivado and Vitis 2020.1 Installations**: [Installing Vivad, Vitis, and Digilent Board Files](https://reference.digilentinc.com/learn/programmable-logic/tutorials/2020.1/installation) guide.
* **Serial Terminal Emulator**: 
* **MicroUSB Cable**

Demo Setup
----------

1. Download the most recent release ZIP archives from the repo's [releases page](https://github.com/Digilent/Cmod-A7-15T-OOB/releases). These files are called "Cmod-A7-15T-OOB-hw-2020.1-1.zip" and "Cmod-A7-15T-OOB-sw-2020.1-1.zip". The -hw- archive contains an exported XPR project file and associated sources for use with Vivado. The -sw- archive contains exported project files for use with Vitis. Both of these files contain the build products of the associated tool.
2. Extract the downloaded -hw- archive. (Do not extract the -sw- archive)
3. Open Vivado 2020.1.
3. Open the XPR project file, found at \<archive extracted location\>/hw/hw.xpr, included in the extracted hardware release in Vivado 2020.1.
4. No additional steps are required within Vivado. The project can be viewed, modified, and rebuilt, and a new platform can be exported, as desired.
5. Open Vitis 2020.1. Choose an empty folder as the *Workspace* to launch into.
6. With Vitis opened, click the **Import Project** button, under **PROJECT** in the welcome screen.
7. Choose *Vitis project exported zip file* as the Import type, then click **Next**.
8. **Browse** for the downloaded -sw- archive, and **Open** it.
9. Make sure that all boxes are checked in order to import each of the projects present in the archive will be imported, then click **Finish**.
10. Connect the Cmod A7 to your computer via the MicroUSB programming cable.	
11. Open a serial terminal application (such as TeraTerm or PuTTY) and connect it to the Cmod A7's serial port, using a baud rate of 9600.
12. In the *Assistant* pane at the bottom left of the Vitis window, right click on the project marked `[System]`, and select **Run** -> **Launch Hardware**. When the demo is finished launching, messages will be able to be seen through the serial terminal, and the demo can be used as described in this document's *Description* section, above.

Next Steps
----------
This demo can be used as a basis for other projects by modifying the hardware platform in the Vivado project's block design or by modifying the Vitis application project.

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [digilent-vivado-scripts](https://github.com/digilent/digilent-vivado-scripts) and [digilent-vitis-scripts](https://github.com/Digilent/digilent-vitis-scripts) repositories.

