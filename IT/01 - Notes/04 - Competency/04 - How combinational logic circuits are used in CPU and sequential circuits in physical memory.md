
# How combinational logic circuits are used in CPU and sequential circuits in physical memory

Major building blocks of CPU 
- Half Adder
- Full Adder

**An adder is a digital circuit that performs addition of numbers.**

#### Half Adder
This adder is used to add 2 single bits.

When we add such 1 bit 2 numbers together, it can be shown as below.

![](../../../assets/Images%201/Pasted%20image%2020221029123220.png)

Since at the last one we have a carry bit of 1 (`10`) we write all the other answers as 2 bit numbers.

> Here the output ‘1’of ‘10’ becomes the carry-out. The result is shown in a truth-table below. ‘SUM’ is the normal output and ‘CARRY’ is the carry-out.

We can represent this addition in a logic circuit using `AND` gate and `XOR` gate like below

![](../../../assets/Images%201/Pasted%20image%2020221029123624.png)

Here, when we give the inputs for x and y as in the truth table, we get 2 outputs as `Carry` and `Sum`. In combination, these two provide the answer of the addition we did. 

This circuit is also represented as this

![](../../../assets/Images%201/Pasted%20image%2020221029123644.png)

This is called the half adder.

If we wanted to increase the number of numbers, we have to increase the number of half adders we use. I.e

- 2 numbers --> 1 half adder
```
0 + 0 = 00
0 + 1 = 01
```
- 3 numbers --> 2 half adders = Full adder

```
0 + 0 + 0 = 0
0 + 1 + 1 = 10
```

and if we increase the number of bits, a Full adder is added for every increasing bit.

- 2 bit 2 numbers --> 2 Full Adders

```
01 + 01 = 010
11 + 01 = 100
```

- 3 bit 2 numbers --> 2 Full Adders

```
000 + 001 = 0001
010 + 100 = 0110
```

#### Full Adder

This Adder is made by using 2 half adders.

| Half Adder     | Full Adder     |
| -------------- | -------------- |
| have 2 inputs  | have 3 inputs  |
| have 2 outputs | have 2 outputs |

![](../../../assets/Images%201/Pasted%20image%2020221029131633.png)

![](../../../assets/Images%201/Pasted%20image%2020221029131826.png)
With 2 half adders an additional `OR` gate is added.

![](../../../assets/Images%201/Pasted%20image%2020221029131756.png)

```
1 and 2 -> 2 half adders
3 -> additional OR gate
```

#### 2-bit Word Adder

![](../../../assets/Images/Pasted%20image%2020240622190741.png)

## Flip Flops

https://www.youtube.com/watch?v=Hi7rK0hZnfc

Flip Flops are logic gates too. Here we can create memory with them. Flip flops can also be considered as the **most basic idea of a Random-Access Memory**  

These flip flops are made by coupling either 2 `NAND` gates or `NOR` gates

![](../../../assets/Images%201/Pasted%20image%2020221029134212.png)

![](../../../assets/Images/Pasted%20image%2020240510200241.png)
> When set or reset is 1, Q changes

![](../../../assets/Images/Pasted%20image%2020240510200333.png)
> When set or reset is 0, Q changes


Here, one thing is different, here the output of one gate is used as an input to the other gate.

![](../../../assets/Images%201/Pasted%20image%2020221029134514.png)

the `Q` output is used as an input for the `f`  (`S NOR Q = F`)output. The same goes for the `F` output. (therefore called sequential circuits)

Because of this behavior one problem occurs. Which is when you try to get the output of one gate, you can't accurately say the value of the other input (which is the output of the other gate). So we get all the possible values which are 0 and 1 and get the output.

![](../../../assets/Images%201/Pasted%20image%2020221029134803.png)

| S   | R   | State     |
| --- | --- | --------- |
| 0   | 0   | Unchanged |
| 0   | 1   | Reset     |
| 1   | 0   | Set       |
| 1   | 1   | Unstable  |

Here, since we can't say the accurate value of `Q` to get as an input, we consider both possible values as 2 scenarios.

Once that's considered, after it goes through the 2nd cycle, if the original value of `Q` doesn't change and stays the same, we call that State as `Unchanged`

```
IF (S,R) = (0,0) output would remain unchanged
```

![](../../../assets/Images%201/Pasted%20image%2020221029134953.png)

- when `Q = 0`

![](../../../assets/Images%201/Pasted%20image%2020221029135058.png)

- when `Q = 1`

![](../../../assets/Images%201/Pasted%20image%2020221029135201.png)

Here the value we considered stays the same. So the state is `Unchanged`

In the next stage it's reset.

```
If (S,R) = (0,1), no matter the 1st output, the next output would be 0
```


![](../../../assets/Images%201/Pasted%20image%2020221029135300.png)

- when `Q = 0`
![](../../../assets/Images%201/Pasted%20image%2020221029135528.png)

In the first instance, we consider Q as 0. So is the 2nd instance

- when `Q = 1`

![](../../../assets/Images%201/Pasted%20image%2020221029135710.png)

In the first instance, we consider Q as 1. But in the 2nd instance it becomes 0

The 3rd stage is reset, this means regardless what the output is in the first time, the last output is going to be 1.

![](../../../assets/Images%201/Pasted%20image%2020221029135857.png)


There are 2 types of logic gates
1. Combinational circuits
2. Sequential circuits


## Combinational circuit

**A combinational circuit is a circuit in which the output depends on the current input**. I.e Encoders,  Decoders

- In combinational circuits, the output depends on the levels present at inputs
- A combinational circuit can have an n number of inputs and m number of outputs.
- The **previous state of input does not have any effect** on the present state of the circuit.
- The combinational circuit do not use any memory.


## Sequential circuit

**A sequential circuit is a logical circuit, where the output depends on the present value of the input signal as well as the sequence of past inputs** I.e Flip Flops

- Based on a concept called feedback
- Output depends not only on the current inputs but also on the previous inputs
- Used for storage (SRAM) and timing
- Generalization of Flip-flops


| Combinational                        | Sequential                                             |
| ------------------------------------ | ------------------------------------------------------ |
| Output depends on the present inputs | Output depends on the present input and the past state |
| No memory                                     | Pocesses memory                                                        |

