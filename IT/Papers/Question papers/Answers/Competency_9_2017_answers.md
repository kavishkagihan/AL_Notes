- MCQ
1. 5
2. 1
3. 5
4. 4
5. 4
6. 5
7. 2
8. 3
9. 3


10.a) ![[../../../../assets/Excalidraw/2017_AL_10_a]]
b) 

```python
pst_val = int(input("Past readiing > "))
prt_val = int(input("Present readiing > "))
hs_num = int(input("Household number > "))

if (prt_val - pst_val) > 64:
    print(f"Bill for {hs_num} is { (64 * 5) + (prt_val - pst_val) * 10}")
else:
    print(f"Bill for {hs_num} is { (prt_val - pst_val) * 5}")
```

c)
```python
def a(a,b,c,d):
	with open('deb.txt', 'a') as f:
		f.write(f"{a} {b} {c} {d}")
```