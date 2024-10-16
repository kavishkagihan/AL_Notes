- 2018
![](../../../assets/Images%201/Pasted%20image%2020220924141800.png)

a) 

| A   | B   | C   | Z   |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 0   |
| 0   | 1   | 0   | 1   |
| 1   | 0   | 0   | 0   |
| 0   | 1   | 1   | 0   |
| 1   | 0   | 1   | 1   |
| 1   | 1   | 0   | 1   |
| 1   | 1   | 1   | 1   |

b)
```
SOP
x = (A'BC') + (AB'C) + (ABC') + (ABC)

POS
x = (A+B+C).(A+B+C').(A'+B+C).(A+B'+C')
```

![](../../../assets/Images%201/Pasted%20image%2020221001124241.png)

- SOP simplification
```
x = (A'BC') + (AB'C) + (ABC') + (ABC)
x = (A'BC') + (ABC') + (AB'C) + (ABC)
	Distributive Law
x = BC'(A' + A) + AC(B' + B)
	Inverse Law
x = BC'(1) + AC(1)
	Identity Law
x = BC' + AC
```

- POS simplification
```
x = (A+B+C).(A+B+C').(A'+B+C).(A+B'+C')
x = (A+B+C).(A+B'+C').(A+B+C').(A'+B+C)
	Distributive Law
x = A+(B+C . B'+C'). B+(A+C' . A'C)

```

```
x = (A+B+C).(A+B+C').(A'+B+C).(A+B'+C')
	Distributive Law
x = A+B+(CC').(A'+B+C).(A+B'+C')
	Inverse Law
x = (A+B + 0).(A'+B+C).(A+B'+C')
	Inverse Law
x = (A+B + 0).(A'+B'+B+C).(A'+A+B'+C')
	Distributive Law2
x = (A+B+0). A'+B'+(B+C . A+C')

```

- 2019

a) 

| A   | B   | C   | Z   |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 0   |
| 0   | 1   | 0   | 0   |
| 1   | 0   | 0   | 0   |
| 0   | 1   | 1   | 1   |
| 1   | 1   | 0   | 1   |
| 1   | 0   | 1   | 1   |
| 1   | 1   | 1   | 1   |

b)

```
SOP
z = (A'BC) + (ABC') + (AB'C) + (ABC)


```

```
POS
z = (A+B+C).(A+B+C').(A+B'+C)

```