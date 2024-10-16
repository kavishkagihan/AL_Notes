
# Analyzes basic digital logic gates in term of their unique functionalities.

## Basic Logic Gates

### XOR

Exclusive OR, if inputs are different to each other, this returns 1, else 0

![](../../../assets/Images%201/Pasted%20image%2020220917121950.png)

![](../../../assets/Images%201/Pasted%20image%2020220917122015.png)

- Truth table with 3 inputs

Here when you get 3 inputs (S1, S2,S3) the method you simply the inputs are as `(S1 xor S2) xor S3`
The output of `S1 xor S2` is then xored with `S3`. All 3 aren't xored at the same time.

![](../../../assets/Images%201/Pasted%20image%2020220917123528.png)
### XNOR

Complement for XOR

![](../../../assets/Images%201/Pasted%20image%2020220917123201.png)

- Truth table with 3 inputs
![](../../../assets/Images%201/Pasted%20image%2020220917123226.png)


## Universal Gates

There are 2 universal gates
	1. NAND
	2. NOR

These 2 gates can be used to create all the other gates

### NAND

##### 1. Creating NOT from NAND

```
NOT(A.A) = NOT(A)
```

![](../../../assets/Images%201/Pasted%20image%2020220917124513.png)


| A   | A   | NOT(A.A) |     | A   | NOT(A) |
| --- | --- | -------- | --- | --- | ------ |
| 1   | 1   | 0        |     | 1   | 0      |
| 0   | 0   | 1        |     | 0   | 1      |


##### 2. Creating AND from NAND

```
NOT( NOT(A.B) . NOT(A.B) ) = A.B
```

![](../../../assets/Images%201/Pasted%20image%2020220917124844.png)


| A   | B   | NOT(A.B) | NOT( NOT(A.B) . NOT(A.B) ) | =   | A.B |
| --- | --- | -------- | -------------------------- | --- | --- |
| 1   | 0   | 1        | 0                          |     | 0   |
| 0   | 1   | 1        | 0                          |     | 0   |
| 1   | 1   | 0        | 1                          |     | 1   |
| 0   | 0   | 1        | 0                          |     | 0   |

##### 3. Creating OR from NAND

```
NOT( NOT(A.A) . NOT(B.B)) = A+B
```

![](../../../assets/Images%201/Pasted%20image%2020220917125201.png)

| A   | NOT(A) |     | B   | NOT(B) |     | (NOT(A).NOT(B)) | =   | A+B |
| --- | ------ | --- | --- | ------ | --- | --------------- | --- | --- |
| 1   | 0      |     | 1   | 0      |     | 0               |     | 0   |
| 0   | 1      |     | 0   | 1      |     | 1               |     | 1   |
| 1   | 0      |     | 0   | 1      |     | 1               |     | 1   |
| 0   | 1      |     | 1   | 0      |     | 1               |     | 1   |

### NOR 

##### 1. Creating NOT from NOR

```
NOT(A+A) = NOT(A)
```

![](../../../assets/Images%201/Pasted%20image%2020220917130226.png)

| A   | NOT(A+A) | =   | NOT(A) |
| --- | -------- | --- | ------ |
| 1   |0          |     | 0       |
| 0    |1          |     | 1       |

##### 2. Creating OR from NOR

```
NOT(NOT(A+B)+NOT(A+B)) = A+B
```

![](../../../assets/Images%201/Pasted%20image%2020220917130430.png)

| A   | B   | NOT(A+B) | NOT(NOT(A+B)+NOT(A+B)) |  =   | A+B |
| --- | --- | -------- | ---------------------- | --- | --- |
| 1   | 0   | 0        | 1                      |     | 1   |
| 0   | 1   | 0        | 1                      |     | 1   |
| 1   | 1   | 0        | 1                      |     | 1   |
| 0   | 0   | 1        | 0                      |     | 0   |

##### 3. Creating AND from NOR

```
NOT(NOT(A)+NOT(B)) = A.B
```

![](../../../assets/Images%201/Pasted%20image%2020220917130858.png)

| A   | B   | NOT(A) | NOT(B) | NOT(NOT(A)+NOT(B)) |  =   | A.B |
| --- | --- | ------ | ------ | ------------------ | --- | --- |
| 1   | 0   | 0      | 1      | 0                  |     | 0   |
| 1   | 1   | 0      | 0      | 1                  |     | 1   |
| 0   | 0   | 1      | 1      | 0                  |     | 0   |
| 0   | 1   | 1      | 0      | 0                  |     | 0   |

---
##### Summary
1. NAND
	- NOT = NAND  
		- `NOT(A) = NOT(A.B)`
	- AND  = NAND( NAND . NAND )
		- `(A.B) = NOT( NOT(A.B) . NOT(A.B) )`
	- OR = NAND( NAND . NAND )
		- `(A+B) = NOT( NOT(A.A) . NOT(B.B)) `

2. NOR
	- NOT = NOR
		- `NOT(A) = NOT(A+B)`
	- OR = NOR( NOR + NOR ) 
		- `(A+B) = NOT( NOT(A+B) + NOT(A+B) )`
	- AND = NOR( NOR + NOR )
		- `(A.B) = NOT( NOT(A+A) + NOT(B+B) )`

---

When building circuits in real life, the following elements should be considered
1. Cost
2. Power Consumption
3. Heat generation
4. Physical size
5. Inter-communication speed - Between 2 ICs
6. Intra-communication speed - Inside one IC 


Question:

1. When constructing logic circuits, why do industries prefer to use universal gates rather than using basic gates?

```
Using universal gates instead of basic gates allows circuit designers to simplify the design process by reducing the number of gate types needed. This reduces the complexity of the circuit, making it easier to design, test, and debug.
```
