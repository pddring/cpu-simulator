# HTML5 CPU Simulator (8 bit binary implementation of Little Man Computer)

![Von Neumann CPU Simulator for OCR A Level](https://tools.withcode.uk/cpu/thumb.jpg)

## Summary
This project is a simulation of the Little Man Computer CPU adapted to make it more suitable for OCR A Level students.

## Try it
You can see a live demo of this project here: [tools.withcode.uk/cpu](https://tools.withcode.uk/cpu)

## Features
This CPU simulation allows you to:
- Step through each step of the fetch decode execute cycle
- See which register is affected by each step with an explanation of what's happening
- See how data changes in each register 
- Write & run your own code on the CPU
- Save / Share your code
- View and run example code 

## Background
The Little Man Computer (LMC) model CPU is a brilliant way of introducting students to the fetch-decode-execute cycle that controls how a CPU operates.

The LMC simplifies the insides of a CPU down to just three registers:

- Accumulator: General purpose registers
- Program Counter: Keeps track of the address of the next instruction
- Instruction Register: The current instruction being executed.

For A-Level (my students are studying the OCR course), you also need to be aware of the purpose and function of following CPU components:

- Memory Address Register
- Memory Data Register
- Control Unit
- Arithmetic Logic Unit
- Data Bus
- Control Bus
- Address Bus

I wanted to create a simulator that would incorporate all of the above whilst still remaining as simple as possible.
The aim of this project is to explain what happens at each stage of the fetch, decode, execute cycle in terms of the flow of data between registers and busses.

## Key differences from LMC
A Little Man Computer CPU has 99 mailboxes (memory locations) which can each store a signed integer between -999 and 999.
Instructions on a LMC are stored as 3 digit denary numbers where the most significant digit represents the instruction and the least significant two digits are the address.

E.g. in LMC,
`LDA 1` assembles to the command `501`

which breaks down to:
  `5`  (Load) from address `01` (Mailbox 1)
  
This CPU has 8 bit registers. The most significant 4 bits contain the opcode and the least significant 4 bits are the address.

E.g. in this CPU, 
`10010001`

splits into the opcode `1001` (or denary 5) and address `0001` (denary 1)

This means also meads Load from memory address 1

The instruction set has been kept the same as the Little Man Computer, but the instructions are encoded in binary rather than denary.

Because addresses can only be stored as a 4-bit nibble, the ram is limited to 16 locations. Each of these store 8 bit values.
In order to be able to cope with negative numbers, integer values in memory are interpreted as signed 8 bit numbers encoded using twos complement.

## Credits
The structure of the processor is based on the diagram in the excellent [Craig'n'Dave youtube videos](https://youtu.be/OTDTdTYld2g?t=22s)
The code uses the following libraries:
- [Bootstrap](http://getbootstrap.com/) for user interface. MIT license.
- [FontAwesome](http://fontawesome.io/) by Dave Gandy for icons. MIT license.
- [jQuery](https://jquery.com/) for DOM manipulation. MIT license.
- [Raphael](http://dmitrybaranovskiy.github.io/raphael/) for drawing annotations. MIT license.
- [ShareThis](https://www.sharethis.com/) for social share buttons. (c) 2017 ShareThis

## See Also
- [CPU Battle Tanks](https://github.com/pddring/cpu-battle-tank/wiki): Control a tank with a Little Man Computer CPU
