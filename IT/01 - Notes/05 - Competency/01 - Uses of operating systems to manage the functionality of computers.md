# Uses of operating systems to manage the functionality of computers

- Why do we need an OS in a computer?

```
Not every computer has an OS. Operating systems are only used when its required to manage differnet tasks. If there is only one task to manage (fans, refrigerators) there is no need of an OS 
```

- What is an Operating System?
```
An OS is a program that controls the execution of application programs and acts as an interface between applications and the computer hardware.
```

- Booting process of the OS

```
1. POST (Power on self start) - check for peripheral devices
2. BIOS in ROM reads Bootable instructions from CMOS (Complementry Metal-Oxide Semiconductor) 
3. Finding the bootable disc and the sector to load the OS
4. Bootstrap loader loads the OS from the hard disk 
```

**Difference between general purpose computers and embedded systems**

| General purpose               | Embeded systems          |
| ----------------------------- | ------------------------ |
| Upgrades are done             | No upgrades are done     |
| Complicated user interactions | Simple user interactions |
| More resources are used       | Less resources are used  |

There are 3 main roles that an OS should provide.
1. **OS provides a virtual machine**
	- hides complex hardware details
	- provides a nice interface to application software and end users.            
2. **OS manages computing resources (software and hardware)**
	- Keeps track of resource usage
	- Grants/ revokes permissions for resources (protection of program from other programs)
3. **OS allow executing applications**

#### Interactions between hardware components


![](../../../assets/Images%201/Pasted%20image%2020221105130402.png)

#### How we interact with the OS

![](../../../assets/Images%201/Pasted%20image%2020221105130153.png)


### Evolution of OS

1. No OS (late 1940s – mid 1950s) 
2. Simple batch system (mid 1950s) 
3. Multi-programmed batch systems (1960s) 
4. Time sharing systems (1960s) 
5. Multi-programmed time sharing systems

#### No OS

- Used in the **1st generation computers**
- Programmers and users directly interacted with the hardware
- **Manual program scheduling**
	- We have to schedule manually which program execute first and next
- **Uniprogramming**
	- executing one program at a time

![](../../../assets/Images%201/Pasted%20image%2020221112121304.png)
- **Serial Processing** 
	- processing programs one after another (still only one program can be loaded to the RAM at one time)
	- due to this loading time is high (loaded bit by bit)

##### Problems 
- One of the main problem is that the **processor is sat idle when loading programs and doing I/O**
- Having to interact with computer hardware directly.

####  Simple Batch System

- Used in the **2nd generation of computers.**
- These computers were built to maximize the processor utilization (By solving the problem had with No OS)
- First batch OS was **developed by General Motors** company
- OS loads and executes a new program from a batch of programs once the current program is ended.
- Batch of programs were recorded in a magnetic tape
- output of the current executed program is written to another tape.

###### Features of simple batch system
- No direct access to computer hardware
- Serial processing
- Uniprogramming
- High response time
- Processor sat idle during I/O

##### Problems
- Compared to the No OS, **loading time problem** and **direct access** problems are solved in this system. Still, the problem of processor sat idle when doing I/O remains. To resolve this next system was implemented.


#### Multi-Programmed batch Systems

- **Central theme of modern OS** 
- **Introduced in** **3rd generation** to minimize the processor idle time during I/O.
- **Memory is partitioned** to hold multiple programs
- When current program waiting for I/O, OS switches processor to execute another program in memory.

![](../../../assets/Images%201/Pasted%20image%2020221105133636.png)

- If memory is large enough to hold more programs, processor could keep 100% busy and can maximize the processor utilization

##### Problems
- Still there is a problem with high response time(introduced time-sharing system as a solution)

#### Time Sharing System

- Introduced to **minimize the user response time** and maximize the user interaction during program execution **in 3rd generation of computers**.
- OS switches processor from one program to another after a certain time quantum (**context switching**). 
- If the certain program doesn't finish execution in the time given, it will have to wait till the next time comes.
- Enables to share the processor time among multiple programs

![](../../../assets/Images%201/Pasted%20image%2020221105140344.png)

##### Advantages of time-sharing
- Each program gets equal opportunity
- Less chance of duplication of software
- CPU idle time can be reduced.

#### Multi Programming Time Sharing Systems

- This is kind of the addition of both concepts used in **muti-programmed batch system** and **time sharing system**
- **When current program wants to do I/O, OS switches processor to execute another program in memory.**

![](../../../assets/Images%201/Pasted%20image%2020221114125327.png)
- Used in **Modern OS.**
- Context switching is used.

So in theory these systems were built  to get the most usage out of the CPU one after the other.

### Classification of Operating Systems

1. Different types of Operating Systems (Based on the users)
	- Single user - Facilitates single user to use the system at a time
		- Single-task - For Palm handheld computers, Ms-DOS
		- Multi-task - Microsoft's Windows, Apple MacOS
	- Multi User-Facilitates multiple users to use the system at a time
		- Multi-task -  Unix server

2. Different types of Operating Systems (Based on Number of tasks)
	- Single Task – Executes only one program at a time
	- Multi Task - Executes multiple programs at a time


##### Multi-threading

```
A thread is also called a sub process. A process can use threads to divide its processes to execute them simultaneously.
```

![](/assets/Images%201/Pasted%20image%2020221105141536.png)


##### Real Time systems

- OS is designed to run applications with **very precise** timing and with a high **degree of reliability**.
- The main objective of real-time operating systems is **their quick and predictable response to events**.
- Examples:
	- Airbag control system in a car
	- Medical equipments
	- Nuclear plant control system