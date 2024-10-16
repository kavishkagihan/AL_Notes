
# Explores how an operating system manages the memory resources

- What is memory management?
```
Partitioning of memory is called memory management.
```
### Types of partitioning
There are 2 types of partitions
1. Fixed partitioning
2. Dynamic partitioning
#### Fixed Partitioning 

- Partitions memory into fixed static portions during the design of the system
- Fixed number of processes can use memory at a time
- Two kinds of fixed partitioning
	- Equal size fixed partitioning
		![](../../../assets/Images%201/Pasted%20image%2020221126122048.png)
		- Strengths  - Simple to implement, Minimum overhead (fewer activities for the OS)
		- Weaknesses - If process is too small it may use all the space (**internal fragmentation**), Large processes are required to redesign, 
	
	- Unequal size fixed partitioning
		![](../../../assets/Images%201/Pasted%20image%2020221126123532.png)
		- Incoming process is directed to the smallest available partition that is big enough to load it
		- Every partition has a separate queue to hold the swapped out processes suitable for that partition
		- Strength - Reduces Internal fragmentation.
		- Weaknesses - If process is smaller than the smallest available partition, it may not utilize the partition space efficiently, If process is larger than the largest partition in the system, **program is required to redesign**., There can be a process waiting in the queue to be processed

#### Dynamic Partitioning

- Partitions memory dynamically based on the size of incoming processes.
- No internal fragmentation happens because the exact amount of memory needed for the process is allocated
- Strengths
	- No internal fragmentation
	- No need to redesign programs
	- Variable number of processes can use memory at a time
- Weaknesses                       
	- Dynamic memory allocation overhead (OS uses the processor to partition the memory itself before loading the programs) (Overhead simply means using processor time by OS to do tasks that aren't exclusively related to OS)
	- External Fragmentation occurs due to swapping actions by the time passes. 
- Solution
	- To solve this, all the processes in memory are moved to one end, leaves a large free space at the other end. (**periodical compaction**)
	- Processing overheads

#### External Fragmentation

![](../../../assets/Images%201/Pasted%20image%2020221126130456.png)

> Say the OS swap in `Process 1` which is 20 MB, `Process 2` which is 14 MB and `Process 3` which is 18 MB at first. Then `Process  3` is swapped out after execution is done.  Then another process of 4MB is swapped in while `Process 1` swaps out and another process of 14 MB fill that space. Now  the memory has 6MB, 6MB and 4MB space left respectively. Now if there is a 12 MB process that needs to be loaded to the memory, it can't be done as there is no space block with 12 MB memory even though it has enough memory separately (6 + 6 + 4 = 16MB) This is called **External Fragmentation**

(When unusable space is left inside a group-sized container, its internal fragmentation, while if it happens outside its external fragmentation.)

### Virtual Memory

When the memory in RAM isn't enough to store the currently executing processes, a part of the HDD is used to store those processes. That is called Virtual memory.
Even though the processes are stored in the HDD, **they are never executed** in there. Those programs are again loaded to RAM portion by portion and then gets executed.  

There are 2 ways that the RAM loads such portions from Virtual Memory
1. Segmentation
2. Paging

#### Segmentation

- Similar to dynamic partition
- This method divides processes to segments based on thier subroutines (functions defined inside)
- Those segments are loaded to RAM in any place available.
- Features
	- No internal Fragmentation
	- External Fragmentation is possible but very less
	- System overheads

####  Paging

- Most popular virtual memory technology.
- Divides processes into small, equal size **pages** (default in most often - 4KB).
- Partitions memory into page size blocks (**page frames**).
- Transfers pages from disk to page frames in memory.
- When a frame is no longer needed, it's moved back to disk.
- Features
	- No external fragmentation


### Address translation

When paging happens, the process portions stored in the Virtual Memory (HDD) are moved to RAM. These portions stored in the HDD has a certain memory address. This address is called the `logical address` These logical addresses are moved to the page frames in the RAM. These page frames have a certain address as well. Those addresses are called `physical addresses`

```
pages (in HDD) -> logical addresses / virtual addresses
frames (in RAM) -> physical addresses 
```

These addresses are mapped together so that the processor know which portion of the process was moved to which page frame in the RAM. This process of **translating logical addresses to physical addresses is known as Address Translation**

There are 2 things that helps with this process.
1. Hardware - Memory Management Unit (MMU) in the processor
2. Software - Page table that includes the mappings of the addresses


![](../../../assets/Images%201/Pasted%20image%2020221210125520.png)

> To process the 455th byte, the processor needs to look up the Page Table and go to `Page 2`. As the Page Table says, the 455th byte is stored in `Frame 8` 

The offset is also called as `Displacement`

![](../../../assets/Images%201/Pasted%20image%2020221210132925.png)


![](/assets/Images%201/Pasted%20image%2020221210133522.png)
- Find the no of  pages by dividing the **memory of the program** from the page size 
- Find the no of  frames by dividing the **memory of the RAM** from the page size 

###### Example case

Say you have a program of 64 KB memory and your RAM is 128 KB and the system page size is 8 KB. 

1. Now if you want to find the **no. of memory pages** that this program can have, you need to divide the memory of the program from the system page size `64 / 8 = 8`
2. Same as above, if you want to find the **no. of frames** that the RAM can have, need to divide the memory of the RAM from the system page size `128 / 8 = 16`
3. According to this, the first page has 8192 bytes, meaning that the 0th page is from bytes 0 to 8191 and the 1st page is from 8192 to 163833 and so on.
4. To find the **no. of bits used to represent the page number in the logical address**, you need to write the no of pages as power of 2  `8 = 2**3`. This means that you need 3 bits to represent the page no.
5. To find the **no. of bits used to represent the frame number in the logical address**, you need to write the no of frames as power of 2  `16 = 2**4`. This means that you need 4 bits to represent the frame no.
6. To find the **no. of bits needed to represent the offset (Displacement)**, you need to represent the page size in bytes (as a power of 2) `8 KB = 8 * 1024` -> `8 = 2**3 * 2**10 = 2**13`. This means 13 bits are used to represent the offset
7. The total bits used to represent the virtual address is `no. of bits in page no + no. of bits in offset` -> `3 + 13` which is `16 bits`.
8. Similarly. the total bits used to represent the physical address is `no. of bits in frame no + no. of bits in offset` -> `4 + 13` which is `17 bits`

Now we can make the logical and physical addresses based on these.

1. Let's say you need to find the logical address of 9000, For that you have 2 ways, you either,
	-  convert 9000 to binary, add 0's to front so that it becomes a 16-bit address ,get last 13 bits as the offset and the first 3 bits as the page number. 
		![](../../../assets/Images%201/Pasted%20image%2020221217131325.png)
	- or subtract the no of bytes in a system page size (which in this case is 8192 (`8 * 1024`)) from 9000, get the binary of the difference as offset after filling with zeros so it becomes 16 and get 1 as 9000 lies under page 1
		![](../../../assets/Images%201/Pasted%20image%2020221217131812.png)
	


---
## Input and output Device Management

#### Device driver

Device driver is a software. When a new  device is introduced to the OS, the certain device driver must be installed in order for the OS to be able to communicate with it. Device drivers depends on both the hardware and the operating system loaded in to the computer

#### Spooling

Spooling is an acronym for `simultaneous peripheral operations on line`.  Spooling refers to putting data of various I/O jobs in a buffer. This buffer is a special area in memory or hard disk which is accessible to I/O devices. There are certain things that the OS does relate to spooling.
1. Handles I/O device data spooling as devices have different data access rates.
2. Maintains the spooling buffer which provides a waiting station where data can rest while the slower device catches up.
