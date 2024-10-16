
# Examines PC memory system to identify different types of memory and their main characteristics.

##### Memory hierarchy

This memory hierarchy mainly divides into 2
	1. External Memory/ Secondary memory
		- Memories which **aren't accessible directly** by the CPU are called secondary memory
	2. Internal memory / Primary memory
		- Memories which **are accessible directly** by the CPU are called primary memory

##### Characteristics of Memory Hierarchy Design

- Capacity
- Access Time
- Performance
- Cost per bit

![](../../../assets/Images%201/Pasted%20image%2020220815192248.png)

![](../../../assets/Images%201/Pasted%20image%2020220815192440.png)

##### Different types of memory and their characteristics

Another way to group memory is:
	1. Volatile memory - Memory is not permanent
	2. Non-volatile memory - Memory is permanent


![](../../../assets/Images%201/Pasted%20image%2020220815193110.png)

###### Cache memory

There are 3 types of cache memory
1. Level 1 
	- extremely fast, but relatively small
	- usually embedded in the processor chip			
2. Level 2
	- often more capacity than L1
	- located on the CPU or on a separate
3. Level 3 
	- works to improve the performance of L1 and L2
	- significantly slower than L1 or L2
	- but usually double the speed of RAM

![](../../../assets/Images%201/Pasted%20image%2020220815193957.png)

![](../../../assets/Images%201/Pasted%20image%2020220815194014.png)

###### RAM
 - Main memory
 - Directly accessible by the CPU and so called Volatile
 - s fast and expensive
 - Two technologies are used in RAM
	 1. Static RAM
		 - memory cell is implemented with a **flip-flop** 
		 - Very fast
		 - Low density
		 - used in cache and register memory
		 - Expensive
		 - Consumes more power and generates more heat
		 - Sometimes used to create main memory (in embedded devices) but not often as DRAM
		 - Use charge to store memory
	 2. Dynamic RAM
		 - memory cell is implemented with a **transistor and a capacitor**
		 - Cheap
		 - High density
		 - Not as fast as SRAM
		 - Consumes less power
		 - One problem with DRAM is that it looses the charge in capacity
		 - Commonly used to create Main memory
		 - Use voltage to store memory

| Criteria                  | SRAM               | DRAM                       |
| ------------------------- | ------------------ | -------------------------- |
| Main Component            | Flip Flops         | Transistors and Capacitors |
| Speed                     | Faster             | Slower                     |
| Density                   | Less dense         | High dense                 |
| Cost                      | Expensive          | Cheap                      |
| Power Consumption         | High               | Low                        |
| Method of storing memory  | as charge          | as voltage                 |
| Places found              | cache and registry | Main memory                |
| Need periodic refreshment | No                 | Yes                        |
| Capacity                  | Low                | High                       |


![](../../../assets/Images%201/Pasted%20image%2020220815194619.png)

- Solution is to refresh the charge periodically (While refreshing, cannot read/write)

###### ROM
- Non-volatile
- Bootup instructions are stored
- Types of ROM
	- MROM
	- PROM
	- EPROM
	- EEPROM

### Synchronous dynamic random access memory (SDRAM)
- An interface synchronous with the system bus carrying data between the CPU and the memory controller hub
- rapidly responding synchronous interface
- **synchronizes with the computer's system clock**

### Questions![[../../../assets/Excalidraw/04 - Examines PC memory system to identify different types of memory and their main characteristics 2023-10-08 13.40.36.excalidraw]]
- [[Q&A Competency 2]]