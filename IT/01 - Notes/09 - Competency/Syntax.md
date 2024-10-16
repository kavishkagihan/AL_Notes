
# Errors

- Semantics errors are errors when the code is syntactically correct but behaves differently as excepted, Could be logical errors.

# Operators

 - Arithmetic

![](../../../assets/Images/Pasted%20image%2020240619155225.png)


 - Assignment 
![](../../../assets/Images/Pasted%20image%2020240619155232.png)![](../../../assets/Images/Pasted%20image%2020240619155327.png)

- Bitwise
https://www.youtube.com/watch?v=PyfKCvHALj8
![](../../../assets/Images/Pasted%20image%2020240619155426.png)

```python
# NOT
>>> a = 60
>>> ~a
-61
```

```python
# Left shift
>>> a = 5
>>> b = 3
>>> a << b
40

bin_5 -> 101.0000
left_shift_by_3 -> 101'000'.0 # Moving the number 3 bits to the left (adding 3 0s)
				-> 101000.0

>>> int("1011000", 2)
40
```

```python
# Right shift
>>> a = 15
>>> b = 3
>>> a >> b
1

bin_15 -> 1111.0
right_shift_by_3 -> 1.'111'0 # Moving the number 3 bits  to the right (removing 3 bits)
				 ->  1.0
>>> int("1", 2)
1	
```

- Precedence

![](../../../assets/Images/Pasted%20image%2020240619155453.png)![](../../../assets/Images/Pasted%20image%2020240619155507.png)

# Lists

- List methods

![](../../../assets/Images/Pasted%20image%2020240619155706.png)

```python
>>> a = [1,2,3]
>>> b = a.copy()
>>> b
[1, 2, 3]
---
>>> a.extend([4,5])
>>> a
[1, 2, 3, 4, 5]
---
>>> c = ["a","b","c"]
>>> c.index("b")
1
---
>>> c.insert(1,"d")
>>> c
['a', 'd', 'b', 'c']
---
>>> c.pop(1)
'd'
>>> c
['a', 'b', 'c']
---
>>> c.remove("a")
>>> c
['b', 'c']
---
>>> h = [5,2,6,1]
>>> h.sort()
>>> h
[1, 2, 5, 6]
>>> g = ["b", "a", "B", "A"]
>>> g.sort()
>>> g
['A', 'B', 'a', 'b']
```
# Tupples

- Tuple methods

![](../../../assets/Images/Pasted%20image%2020240619155825.png)


 # Dictionaries
- Dictionary methods

![](../../../assets/Images/Pasted%20image%2020240619155740.png)


```python
>>> a = {"name": "kavi", "age": 19}
>>> a.get("name")
'kavi'
>>> a['name']
'kavi'
---
>>> for i in a.items():
...     print(i)
...
('name', 'kavi')
('age', 19)

---
```

# File handling


![](../../../assets/Images/Pasted%20image%2020240619160022.png)

- Example
![](../../../assets/Images/Pasted%20image%2020240619160049.png)



# DB connection


![](../../../assets/Images/Pasted%20image%2020240619160234.png)

- Insert data
![](../../../assets/Images/Pasted%20image%2020240619160307.png)

![](../../../assets/Images/Pasted%20image%2020240619160347.png)
> Note that for any command that has to update or add info, you need to use the `mysql.commit()` function to write the changes to the db

- Retrive data

![](../../../assets/Images/Pasted%20image%2020240619160500.png)