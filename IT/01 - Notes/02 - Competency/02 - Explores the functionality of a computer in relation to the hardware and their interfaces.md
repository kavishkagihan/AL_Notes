
# Explores the functionality of a computer in relation to the hardware and their interfaces
#### Input devices

- Input devices
	- Direct entry input devices
		- Magnetic strip reader
		- Bar code reader
		- Smart card reader
	- Pointing devices
		- Mouse
		- Joy stick

###### Advantages of direct entry input device over keyboard
- Automatic capturing of data
- Accuracy - No human errors
- Less time is consumed
- No human involvement is needed

#### System Unit

The system unit, also known as the **system chassis** s a container that houses most of the electronic components that make up a computer system. This contain,
	- System board / Mother board
	- Bus
	- Ports
	- Memory


###### System board
- controls  communications for the entire computer
- contains 3 main components as **sockets, slots, bus lines**
	- Sockets
		- provide a connection point for small specialized electronic parts called **chips** made of silicon
		- used to connect the system board to a variety of different types of chips, including microprocessor and memory chips
	- Slots
		- provide a connection point for specialized **cards** or **circuit boards**
		- I.e wireless networking card
	- Bus lines
		- provide pathways that support communication among the various electronic component

![](../../../assets/Images%201/Pasted%20image%2020220718200132.png)


### Microprocessor/CPU

CPU is contained on a single chip called the **microprocessor**

- It has 3 basic components.
	1. Memory unit (Registers) 
	2. Control unit
		- tells the rest of the computer system how to carry out a program’s instructions
		- directs the movement of electronic signals between memory(RAM) and ALU and between input-output devices and CPU
	3. ALU
			- 2 main operations
				- Arithmetic operations (+. -, \*, /)
				- Logical operations (>. <, =)


- **Chip processing capacities are often expressed in word sizes** (the number of bits processed by the CPU of a computer in a single action) A word is the number of bits (such as 16, 32, or 64) that can be accessed at one time by the CPU
	- 32 bit ⇾ 4 bytes at a time
	- 64 bit ⇾ 8 bytes at a time

- The processing speed of a microprocessor is typically represented by its  **clock speed**. **Clock speed is number of times the CPU can fetch data in a second. **Unit used it ** Hertz** (Hz)

![](../../../assets/Images%201/Pasted%20image%2020220725183843.png)

- Microprocessors can run only one program at a time. Multicore processors can run multiple processors at a time.
	- 2 core → 2 programs at a time. 1 core for Excel. 1 core for word
	- parallel processing is used to divide the tasks in to parts to process it faster
#### Specialty Processors
- Different specialized chips used instead of CPU are specialty processors
	- Coprocessors - specialty chips designed to improve specific computing operations.
	- GPU - Used to process graphics
	- Crypto processors - used in encrypting and decrypting (ATM cards)

- When it comes to CPU compatibility with its motherboard, we need to consider 4 things.
	1. Socket support
	2. Chipset support
	3. Motherboard Wattage support
	4. BIOS support

### Memory
```
Memory is a holding area for data, instructions, and information
```
There are 3 types of memory
	1. RAM
	2. ROM
	3. Flash

Unit used to measure is **Gigabytes**

##### RAM

- Volatile
- Temporary memory are stored
- Fastest memory out of 3 main memory types

###### Cache memory
- Second fastest memory from all (1st is registry memory) 
- Act as a mediator between CPU and RAM
- Store most often accessed data temporarily 
- 3 types of cache memory
	- Level 1 - always inside the processor
	- Level 2 
	- Level 3 - always outside the processor
- Level 2 cache are brought inside the microprocessor, BUT they are **not components of the processor**
	
- RAM can be expanded by inserting an expansion module called **DIMM** **(dual in-line memory module)**
- If still memory is not enough virtual memory is used. (Virtual memory = RAM + HDD)
- Virtual memory is given by the HDD when RAM is not enough

##### ROM

- Non-volatile
- Booting instructions are stored
- 4 types of ROM chip
	- Mask ROM - Can't be programmed or erased, instructions set by the manufacturer are stored
	- PROM - programmable ROM
	- EPROM - Erasable ROM using UV rays
	- EEPROM - Electronic Erasable ROM

- Flash memory chips have replaced ROM chips for many applications.

##### Flash memory
- Combination of RAM and ROM
- Like RAM, it can be updated to store new information
- Like ROM, it does not lose that information when power to the computer system is turned off.
- Bootup instructions are called BIOS (Basic Input Output System)

![](../../../assets/Images%201/Pasted%20image%2020220725202534.png)

- Memory from fastest to slowest
```
Registers
Cache
RAM
HDD
Flash drive
Optical media
Magnetic tape
```


##### Expansion Slots and Cards

- allow users to expand their systems by providing expansion slots on the system board
	- Graphics cards
	- Network Interface cards 

##### Bus lines
- connects the parts of the CPU to each other
- Instructions are transfused within bus as bits (0 and 1)
- **The number of bits that can travel simultaneously down a bus is known as the bus width**
- 64-bit bus lines should be with x64 processor, same goes with 32-bit (compatibility of the buses with the processor)
- 2 types of bus lines
	- System bus - connects the CPU to memory
	- Expansion bus  - connects the CPU to other expansion slots and components

###### Expansion Buses

- USB
	- The current USB standard is USB 3.1
- FireWire buses
- PCI Express (PCIe)
	- used in many of today’s most powerful computers
	- unlike USB, this provides a single path, paths are not shared

###### Ports
```
A port is a socket for external devices to connect to the system unit.
```

#### Storage Devices

There are 2 main types of storage devices
1. Magnetic
2. Optical
3. Solid State

Also, they are divided as follows

1. Fixed internal magnetic HDD
2. External HDD
3. Magnetic tape
4. Optical discs

![](../../../assets/Images%201/Pasted%20image%2020220801183714.png)

DVD-RAM is like an ordinary RAM (but aren't volatile) which can be repeatedly read, written and erased. These are way faster than DVD-RW

6. Flash drive

Developed using electrically erasable programming read only memory (EEPROM)

### Parallel computing
```
Parallel computing is a type of computation in which many programs or processes are done simultaneously
```

```
Parallel processing is breaking down a large process in to smaller pieces and executing them in the same time.
```


![](../../../assets/Images%201/Pasted%20image%2020220801190045.png)

Practical issues / scenarios in parallel computing.
	- Some task might not be divisible
	- Some task may not be able to divide equally.
	- It is necessary to take overhead associated with splitting the task up also into account.

### Grid computing
```
Grid computing is a distributed network of large numbers of computers located in different geographical area connected to solve a complex problem
```

Grid computing is the practice of leveraging multiple computers, often geographically distributed but connected by networks, to work together to accomplish joint tasks.

![](../../../assets/Images%201/Pasted%20image%2020220801192204.png)

I.e a research team may analyze the weather in Gamapaha and another team would analyze in Colombo and Kaluthara, then the results are combined to deliver the full weather report for the western province.  



