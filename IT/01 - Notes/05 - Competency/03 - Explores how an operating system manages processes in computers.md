
# Explores how an operating system manages processes in computers.

```
A Process is a program in execution or a program that can be assigned to and executed by a processor. 
```

### Process and Program
**Process is not a program**. A program may have many processes.

A process consists of,
- Executable codes
- Data needed for execution
- Execution context

###### Similarities 
- Both the program and process have Executable codes

###### Dis-similarities

| Process                        | Program                |
| ------------------------------ | ---------------------- |
| Active                         | Passive                |
| Exists for a limited time       | Exists for longer      |
| Have both data and instructions | Have only instructions |

### Interrupt Handling

```
Interrupt is an event that alters the sequence of execution of processes.
```

- **How to handle interrupts by OS**
```
Generally I/O devices are much slower than processor. Therefore, after an I/O call, processor has to sit idle till the I/O device completes its event. Thus, OS saves execution context of current process in PCB (Process Control Block) and switches processor to execute some other process. When I/O event is completed, I/O device interrupts OS. Operating System then retrieves the execution context of suspended process and switches the processor to resume its execution from where it was suspended.

```

Interrupts can occur either synchronously or asynchronously.
- Synchronous interrupts are triggered by the **system itself**, typically in response to some kind of error or exception. These are **predictable** 
- Asynchronous interrupts, are triggered by **external events**, such as user input or a device requesting access to the system. These are **unpredictable**. 

##### PCB
 ```
PCB is a data structure that is used to store the execution context of a process.  
```
 When a process is made a PCB is also made to store and restore the current state of the process. PCB also **stores the current information about the process**. When a process dies, the PCB also gets removed. PCB is a small space in the RAM that normal users don't have access to.

- **Information Stored in PCB**
	- Identifier 
	- State 
	- Priority 
	- PC - address of the next instruction to be executed
	- Registers - CPU register values associated with the process
	- I/O info - I/O devices assigned to process

![](../../../assets/Images%201/Pasted%20image%2020221119132519.png)


- What are 2 main techniques used to optimize processor utilization?
```
Multiprocgramming
Time sharing
```
> Both of these techniques use context switching

#### Context switching

```
A context switch is the mechanism to store and restore the state or context of a CPU in the Process Control Block so that a process execution can be resumed from the same point at a later time.
```

![](../../../assets/Images%201/Pasted%20image%2020221112135839.png)

### Execution of Processes

When processes are executed with interrupt handling and all that, OS uses a **Process Model** to manage the processes.

#### Two state process model

![](../../../assets/Images%201/Pasted%20image%2020221119130158.png)

![](../../../assets/Images%201/Pasted%20image%2020221119123730.png)

Only have 2 stages
1. `Running` state - Processes that are executing atm.
2. `Not Running` state - Processes that are in the queue to get executed.

> New processes enter into `Not Running` state. After the expiry of time quantum or process wants to do I/O, Operating System interrupts the process in `Running` state and transfers it to Not Running state. Operating System then dispatches another process in Not Running state to `Running` state for execution. Complete/aborted processes exit from `Running` state.

Since all the processes are in **one queue,** the processor can't dispatch other processes till the latest process is **done executing** or **its time of execution for that round is finished (timeout)**. 

##### Problem
Some processes in `Not Running `state may be ready to run, but can be blocked by processes waiting for some I/O event completion.

##### Solution
We can divide the `Not Running` queue to 2 as `Ready` and `Blocked` so that the processor can dispatch them separately without waiting for one to finish.

#### Five State Process Model

![](../../../assets/Images%201/Pasted%20image%2020221119130813.png)

There are 5 stages
1. `New` -  newly created process from the HDD
2. `Ready` - Processes that are in the queue to get dispatched
3. `Running` - Processes that are running atm
4. `Blocked` - Processes that are waiting for I/O
5. `Exit` - Processes that the execution is completed.

##### Problem
Processes in the `Blocked` state maybe **blocked even after their I/O is completed**

##### Solution
Blocked state should be split into groups according to the different I/O actions.

![](../../../assets/Images%201/Pasted%20image%2020221119131208.png)

Now small awaited actions can be dispatched again to the `Ready` state without waiting for long awaited actions to be done.


##### Problem
If all the processes are in blocked, RAM runs out of memory making the processor idle

##### Solution
Move some blocked processes to HDD (to virtual memory)

#### Seven State Process Model

![](../../../assets/Images%201/Pasted%20image%2020221119131629.png)

`New` state is in the HDD as well. Meaning that **new processes are created in the HDD.** `activate` can also be named as `Swapped in`. `suspend` can also be named as `Swapped out`

There are 7 stages
1. `New` -  newly created process from the HDD
2. `Ready` - Processes that are in the queue to get dispatched
3. `Running` - Processes that are running atm
4. `Blocked` - Processes that are waiting for I/O 
5. `Blocked Suspended` - Processes that are blocked waiting for I/O which were moved to HDD to reserve RAM
6. `Ready Suspnded` - Processes that has completed I/O from Blocked Suspend, prioritization (Ready -> Ready suspend), newly admitted processes which aren't sent to RAM as there is no space (New -> Ready suspend)
7. `Exit` - Processes that the execution is completed.

Both these `Ready suspnded` and `Blocked suspended`  are stored in HDD (virtual memory), 

> Blocked -> Blocked suspend (Suspend / Swapped out)
	- When memory in the RAM is not enough, so some of the blocked processes are moved to HDD

> Blocked suspend -> Blocked (Activate / Swapped in)
	- Once RAM has enough space, process is again put into Blocked so that it can complete I/O (I/O can be completed while its in Blocked suspend as well)

> Blocked suspend -> Ready suspend
	- If I/O event gets completed while it's in Blocked suspend, it's put into Ready suspend as it's ready to run

> Ready -> Ready suspend
	 - When prioritization happens, processes that are ready to run are put into Ready suspend, giving place to high priority processes

> New -> Ready suspend
	- While creating the process, if a prioritized process gets created first, other low prioritized once are put in to Ready suspend. 
	- Newly created processes which aren't sent to RAM as there is no space are also sent here


![](../../../assets/Images%201/Pasted%20image%2020221130133028.png)

When no process is ready to run and memory is full, one or more processes are **swapped out** and one or more new or suspended processes are **swapped in**.

```
Ready Suspend or Bloacked Suspend (HDD) --> Ready or Blocked(RAM) [swapped in] (Getting processes to the RAM)
Ready or Blocked (RAM) --> Blocked suspend or Ready Suspend(HDD) [swapped out] (Removes the process from RAM)
```

![](../../../assets/Images%201/Pasted%20image%2020221119131911.png)

> Note that the Blocked and Blocked suspend states are implemented with multiple queues to handle processes waiting for different I/O events.

### Types of Processes

1. ` Processor bound processes` - Spend more time for using processor than doing I/O
2.  `I/O bound processes `– Spend more time for doing I/O than using processor 
3. `Premptive processes` – can be interrupted, suspended the execution and resumed later 
4. `Non–premptive processes` – Cannot be interrupted and continue until process completes its execution or blocked by itself (Real Time processes)

### Process Scheduling
1. `Long term scheduling` – schedules admission of processes, decides degree of multiprogramming
2. `Mid-term scheduling` - schedules swapping function
3. `Short term scheduling (aka dispatchers aka processor scheduling)` – schedules switching of processes between ready and running state (used in context switching, therefore very frequently happens)

![](../../../assets/Images%201/Pasted%20image%2020221119133457.png)

![](assets/Images%201/Pasted%20image%2020221119133548.png)

```
Ready -> Running - Short term
From new -> any - Long term
Ready -> Ready suspend (vise versa) - Mid term
Blocked -> Blocked suspend (vise versa) - Mid term (or any swapping action)
```


Assignments to optimize the processor.
1. `Response Time` -  time between submission of a request and receipt of response
2. `Thoughtput` - number of processes completed per unit time
3. `Turnaround time` – average time from submission of a process to its completion
4. `Waiting time` -time a process spends in ready state.

