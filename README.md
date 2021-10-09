# 65CE816-Softcore
This is a 65CE02 Compatible Softcore with additional Features and Instructions. A lot of inspiration for the added features was taken from the 65C816, making this softcore a kind of hybrid between the 2 CPUSs, hence the name.

It's currently not fully tested but should still be mostly functional. I'm Testing it on my Cyclone II Powered Altera DE2 Dev Board. The CPU takes up <3000 Logic Elements and seems to run fine at 25MHz.

I mostly designed it based on the [Datasheet](http://archive.6502.org/datasheets/mos_65ce02_mpu.pdf) and the [C65 Specification](https://github.com/ProxyPlayerHD/65CE02-Softcore/blob/main/C65%20System%20Specifications%20Preliminary%201991.pdf).

# Software used
[Logisim Evolution](https://github.com/kevinawalsh/logisim-evolution) was used to design, build, and test basic functions of the CPU Itself.

you will need it to open any .CIRC files.

[Digital](https://github.com/hneemann/Digital) was used to rebuild the whole CPU afterwards so that it can be exported to Verilog/VHDL.

you will need it to open any .DIG files.

and [CustomASM](https://github.com/hlorenzi/customasm/) is used as an Assembler to write programs with.

Custom Snyntax Highlighting was also created for Notepad++, it can be modified to fit whatever colors the programmer wants.

.CEA is the Extension used for the Syntax Highlighting, though that can also be changed.

Each of these Programs has their own folder that contains all important files for it. Exception being the "ROMs" folder, which contains the ROM Files for both the Logisim and Digital Circuits. (all files called PLA_* are for Logisim's PLA Components, everything else is for both Logisim and Digital's ROM Components)

# Misc. things

All of the INST_* Files were used to create the Microcode that runs the CPU

* INST_Indexed contains all Instructions and their cycles written out in "Pseudo Micro-Instructions", and what Unique Number each Instruction has.
* INST_All_States lists all unique Micro-Instructions that the CPU can do, and what Micro-Opcode they have (on the left in Hex)
* INST_LIST is a simple list of all Instructions used for Logisim's Text Display below the CPU, so you can see what it is currently Executing.
* INST_Microcode Cycles is very similar to INST_Indexed but the Instructions were made all the same amount of lines for easier conversion to Hex.
* INST_New is a list of all newly added Instructions for a more detailed description please refer to the [6502.org Thread](http://forum.6502.org/viewtopic.php?f=10&t=6639) about this CPU
