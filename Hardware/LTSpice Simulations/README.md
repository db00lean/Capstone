The core functionality of this project lies within the LT3790 buck-boost converter, which allows for high efficiency buck and boost operations on an input source within a specified range. To test the functionality of the IC without creating several PCB revs, we decided to run simulations to ensure "normal" operation of our circuitry prior to ordering boards.

To run the simulation, install LTSpice on your machine and pull the file ```Capstone/hardware/LTSpice Simulations/LT3790_Rev_A.asc```. This is the base simulation file from Linear Technologies for the LT3790 converter. We will build upon this in future revs.

# Simulation Tasks
There are several subtasks within simulating the LT3790 needed to design a fully-functional system that meets our desired goal.

## Understanding The Datasheet
It is vital that all electrical hardware engineers understand the LT3790 datasheet. 
The datasheet is located at ```Capstone/hardware/resources/LT3790_datasheet.pdf```

## Switching Component Selection
For the most efficient operation within our specified ranges of input/output voltage and current, 
we must select appropriate switching MOSFETs and inductors with minimum Rdson and and high enough 
inductor SRF that our maximum switching frequency does not cause the inductor to self-resonate. More to come.

## Current/Voltage Limit Circuitry
The actual circuitry in this portion of the design will differ from the simulation, but we need
to understand how we can modify the voltage and current limits in real-time to adjust our output and 
effectively achieve the universal converter operation. If we can find a way to run code through the 
LTSpice simulation, we may be able to model how the firmware will integrate with the LT3790.

## External Converter Component Selection
A much easier task as we can use what is provided in the component selection portion of the datasheet to
select additional external components around the LT3790.

## Add A Second Converter
For dual-output, we need to add a second converter in the output path of the first. More to come after
fully simulating the base design.

## Add Remaining External Components
Aside from the MCU and firmware related components, we also can simulate the other ICs and components within 
the main power path. More to come.
