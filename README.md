# procto32
RISC-V Single Cycle Processor

In this project, we design a RISC-V single-cycle processor from scratch, exploring each of its essential components. A single-cycle processor executes every instruction in one clock cycle, making it straightforward but less efficient than more complex multi-cycle designs. The RISC-V processor is an open-source instruction set architecture (ISA) known for its simplicity, modularity, and extensibility, making it ideal for learning and research purposes.
Main Components of the Single-Cycle RISC-V Processor:

Program Counter (PC):
The Program Counter holds the address of the current instruction being executed. After each cycle, it increments to point to the next instruction unless altered by jump or branch instructions.
Instruction Memory:

This module stores the machine instructions of the program. The PC fetches the current instruction from this memory. The fetched instruction is then decoded to control the operation of the processor.
Register File:

The register file contains 32 general-purpose registers (x0 to x31). It allows reading two registers and writing one register simultaneously. The register at x0 is hardwired to zero, as per RISC-V convention.
ALU (Arithmetic Logic Unit):

The ALU performs arithmetic and logical operations, such as addition, subtraction, AND, OR, and comparisons. The ALU's operations are determined by control signals based on the instruction type (e.g., R-type, I-type).
Control Unit:

The control unit generates signals to coordinate the flow of data within the processor. It interprets the opcode of the fetched instruction and sets the control signals to drive the ALU, memory access, and data routing in multiplexers.
Data Memory:

Data memory is used to perform load and store operations. It reads data from memory on load instructions and writes data to memory on store instructions, based on the address computed by the ALU.

About RISC-V:
RISC-V (Reduced Instruction Set Computer – V) is an open-source ISA that is designed to be simple and flexible. It supports various extensions (e.g., integer, floating-point, atomic) and has gained popularity for educational purposes, research, and even commercial applications.
