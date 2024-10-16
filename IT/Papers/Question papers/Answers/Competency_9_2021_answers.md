- MCQ
1. 5
2. 1
3. 2
4. 2
5. 2
6. ? (13)
7. 2

8. a)
![[../../../../assets/Excalidraw/2021_8_a_AL]]

b)

```python
1. num
2. num == 0
3. factorial = factorial * i
4. factorial
```

c)

```
2
```

9. a)

```python
calculate_average_age = lambda L, k: sum(filter(lambda age: age < k, L)) / len(list(filter(lambda age: age < k, L)))
```

```python
def calculate_average_age(L, k):
    count = 0
    total_age = 0

    for age in L:
        if age < k:
            total_age += age
            count += 1

    else:
        return total_age / count
```
b)

i)
```
4
```

ii) 

```
To find the common values that both of these lists have
```

iii)

```python
count_common_values = lambda L1, L2: sum(map(lambda value: 1 if value in set(L2) else 0, set(L1)))
```

```python
def count_common_values(L1, L2):
    common_count = 0

    for value in set(L1):
        if value in set(L2):
            common_count += 1

    return common_count
```

