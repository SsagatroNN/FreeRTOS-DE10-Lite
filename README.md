# FreeRTOS-DE10-Lite
A repository containing the necessary includes and configurations to run FreeRTOS on NIOS 2 using DE-10 Lite.


## Guide

- Create a Quartus project containing an SRAM-Controller, On-chip memory, and a timer named `sys_clk`. Other modules may be added depending on the application.
- Correct the pin assignments to fit those found in the `.qsf` file in this repository.
- Create a new software project using the NIOS 2 Eclipse plugin.
- Add the `include` files in this repo to the project and add them to the project including directories.
- Add the `FreeRTOSCOnfig.h` and memory management source file to the project. 
- Add the source and header files in `./portable/GCC/Nios2` to project.
- That's it ! You can now include FreeRTOS.h in your main file and use it freely.

## Note
Although tasks can now be created. It is advised not to deploy more than two tasks in order to avoid performance issues.
