# Explores the Von-Neumann Architecture

#### Processor
```
A processor is a digital device that can perform one or more computations involving multiple steps
```

###### Components of the processor
- Control Unit
- Storage Unit
- ALU
- Internal interconnection - move data and instructions among other internal components
- External interface - connect external device (devices in the mother board I.e RAM, cache memory)

![](../../../assets/Images%201/Pasted%20image%2020220801193857.png)

### Computer Architectures

##### Von Neamann Architecture

- by **John Von Neumann**
- **Stored program concept** is introduced by him  
- Bus line is **shared to access both instructions and data** (both instructions and data cannot be accessed at the same time)
- Therefore, bus becomes a bottleneck (von Neumann bottleneck)
- Even this **results in  performance lack**, **present day computers uses this** as it's **simple and inexpensive**

![](../../../assets/Images%201/Pasted%20image%2020220801194617.png)


##### Major components of Von-Neumann architecture

![](/assets/Images%201/Pasted%20image%2020220808183459.png)

The programs are stored in RAM, CPU fetches memory from RAM at a time and executes them.

1. CPU
	1. CU
	2. ALU
2. Memory register
	- Hold instructions and data, storage locations 
	- Registers help to access memory faster making the processor efficient. 
	1. **Program Counter** (RIP)
		- address of the next **instruction** to run is stored in this register
	2. **Instruction Register**
		- holds the instruction currently being executed
		- located in Control Unit in CPU
	3. **Memory Address Register**
		- stores the **address of the** **data** which is fetched by the CU and sent from the ALU
	4. **Memory Data Register** (MDR)
		- stores the **data** being transferred to and from the immediate access storage (cache) 
		- also know as memory buffer register
	5. **General purpose registers**
		- used to store temporary data
		- Supports two operations such as fetch and store
		- used either by programmer or by a user
	6. **Floating point registers**
		- large enough to store floating point value


### Programming with registers

###### Bus

```
Bus is a group of conducting wires which carries information which connects all the peripherals to the microprocessor.

```

![](../../../assets/Images%201/Pasted%20image%2020220815184421.png)


There are 3 types of busses.
	1. Address bus - carries addresses
	2. Data bus - carries data and instructions
	3. Control bus - carries control signals (writing, reading, storing instructions, Opcode fetch)

#### Fetch-Decode-Execution Cycle
- Basis of programmable processors
- Allows processor to move through program instructions automatically
- Implemented in processor hardware
- Run by the operating system
- If no further instructions are there,  endless loop automatically runs to keep the cycle going.
- Its never stopped unless the computer is powered off


![](../../../assets/Images%201/Pasted%20image%2020220815185422.png)


![](../../../assets/Images%201/Pasted%20image%2020220815185511.png)

1. Control unit fetches instructions from memory
2. Control unit converts instructions to command and feeds to ALU
3. ALU executes the commands (not instructions) and sends data to Main memory
4. Main memory stores the given data from ALU for future use.


![](../../../assets/Images%201/Pasted%20image%2020220815190218.png)

![](../../../assets/Images/Pasted%20image%2020231013164727.png)

##### Multi-core processors

 Need of multi-core processor
	 - Can run a program by dividing some parts. So it gets executed fast
	 - It enables parallel programming
	 - To get the high performance from a single machine


