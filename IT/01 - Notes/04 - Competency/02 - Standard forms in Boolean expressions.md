# Standard forms in Boolean expressions


### Boolean algebra

Just like normal algebra, in boolean algebra as well we can do different operations. There are 3 different operators we can use in boolean algebra
	1. bar (`-`) - Not or negation (`A'`)
	2. dot (`.`) - Anda
	3. plus (`+`) - Or

Only these 3 basic operations are used with boolean algebra, if you want to make an operation like XOR we need to use these to make it. XOR like operations can't be applied directly.


### Boolean Laws

Frequently, a Boolean expression is not in its simplest form

```
2x + 6x
```

So we can simplify them to make them be in the simplest form

```
2x + 6x = 8x
```

Like we did with mathematical expression, we can simplify boolean expressions too. For that some laws should be used.


![](../../../assets/Images%201/Pasted%20image%2020220924122957.png)

Table is just to refer, not to study. Following laws should be studies.

#### Idempotent Law

If same input is put into an operation, the simplified answer is the input itself.

```
A . A  = A
A + A  = A
A' . A' = A'
A' + A' = A'
```

![](../../../assets/Images%201/Pasted%20image%2020220924124001.png)


#### Identity Law

| 1   | A   | 1.A =A |     | 1   | A   | 1+A=1 |
| --- | --- | ------ | --- | --- | --- | ----- |
| 1   | 1   | 1      |     | 1   | 1   | 1     |
| 1   | 0   | 0      |     | 1   | 0   | 1     |

| 0   | A   | 0.A =0 |     | 0   | A   | 0+A=A |
| --- | --- | ------ | --- | --- | --- | ----- |
| 0   | 1   | 0      |     | 0   | 1   | 1     |
| 0   | 0   | 0      |     | 0   | 0   | 0     |


![](../../../assets/Images%201/Pasted%20image%2020220924125116.png)


#### Inverse/Complement Law

| A   | A'  | A.A'=0 | A+A'=1 |
| --- | --- | ------ | ------ |
| 1   | 0   | 0      | 1      |
| 0   | 1   | 0      | 1      |

![](../../../assets/Images%201/Pasted%20image%2020220924125225.png)

#### De Morgan’s Law

Break the bar and change the operator

```
(A.B)' = A' + B'
(A+B)' = A' . B'
```

![](../../../assets/Images%201/Pasted%20image%2020220924125309.png)


#### Double Complement Law

| A   | A'  | A'' |
| --- | --- | --- |
| 1   | 0    | 1    |
| 0    | 1    | 0    |

![](../../../assets/Images%201/Pasted%20image%2020220924125430.png)


#### Commutative Law

```
A.B = B.A
A + B = B + A
```


![](../../../assets/Images%201/Pasted%20image%2020220924125445.png)

#### Associative Law

```
A (B.C) = (A.B).C = (A.B.C)
```

![](../../../assets/Images%201/Pasted%20image%2020220924125527.png)

```
A + (B+C) = (A+B) + C = (A+B+C)
```

![](../../../assets/Images%201/Pasted%20image%2020220924125518.png)


#### Distributive Law

```
A (B+C) = AB + AC --> like bracket opening
```

![](../../../assets/Images%201/Pasted%20image%2020220924125544.png)

#### Redundancy Law/ Absorption Law

| A   | B   | AB  | A+AB=A |
| --- | --- | --- | ---- |
| 1   | 1   | 1    |  1    |
| 0   | 0   |  0   |   0   |
| 1   | 0   |   0  |    1  |
| 0   | 1   |    0 |     0 |

![](../../../assets/Images%201/Pasted%20image%2020220924125634.png)


| A   | B   | A'  | A'B | A+A'B | A+B |
| --- | --- | --- | --- | ----- | --- |
| 1   | 0   | 0   | 0   |   1    | 1    |
| 0   | 1   | 1   | 1   |    1   |  1   |
| 1   | 1   | 0   | 0   |     1  |   1  |
| 0   | 0   | 1   | 0   |      0 |    0 |


![](../../../assets/Images%201/Pasted%20image%2020220924125832.png)

Also,
```
A' + AB = A' + B
```

Also,
```
AB' + ABC = A(B' + BC) = A(B' + C) = AB' + AC
```

