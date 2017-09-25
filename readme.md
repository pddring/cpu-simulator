# cpu-simulator
HTML5 CPU Simulator (8 bit binary implementation of Little Man Computer)

![Von Neumann CPU Simulator for OCR A Level](https://tools.withcode.uk/cpu/thumb.jpg)

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

You can see a live demo of this project here: [tools.withcode.uk/cpu](https://tools.withcode.uk/cpu)
