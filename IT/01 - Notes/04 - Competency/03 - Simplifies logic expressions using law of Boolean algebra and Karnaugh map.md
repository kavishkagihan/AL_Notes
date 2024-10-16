# Simplifies logic expressions using law of Boolean algebra and Karnaugh map

There exist two standard forms of Boolean expressions
	1. SOP - Sum of Product - `AB + BC`
	2. POS - Product of Sum - `(A+B).(B+C)`

#### SOP - Sum of products (`(x.y)+(x.y)`)


Two or more product terms are summed by Boolean summation.

When a truth table is made, if the output is 1 (also known as min terms) those terms are taken as products are added together

```
A + B = Z
```

| A   | B   | Z   |
| --- | --- | --- |
| 0   | 0   |  0   |
| 1   | 0   |   0  |
| 0   | 1   |    1 |
| 1   | 1   |     1|

Here 3rd and 4th entries have the output 1, so these are taken for the SOP expression. When writing the expressions, 0 values should be turned to 1 used a bar (`'`) 

```
x = (A'B) + (AB)
```


#### POS - Product of sums (`(x+y).(x+y)`)

When a truth table is made, if the output is 0 (also known as max terms) those terms are taken as sums and multiplied together

In the above table, 1s and 2nd entries have the output 0, so these are taken for the POS expression. When writing the expressions, 1 values should be turned to 0 used a bar (`'`) 

```
x = (A + B).(A' + B)
```


# Standardizing a boolean expression
In a standard boolean expression, all the terms in the expression should have all the variables

#### SOP standardizing with inverse law (A' + A)

```
A + BC               --> not standard
ABc + AB'C + A'BC'   --> standars
```

What we do is that for the missing variable (I.e `D`), we use the inverse law and get `D' + D` which results in 1 (cuz 1(ABC) = ABC so makes no difference) and use distributive law to the term which doesn't have `D`. Then that will result 2 terms with `D'` and `D` 

![](../../../assets/Images%201/Pasted%20image%2020221008124417.png)

Same method is done to all the terms until all variables are in all terms

This is done for some reasons
	 - It's easy to use a standardized expression to use the karnough map method
	 - When constructing truth tables its important to have the expression in standard format

#### POS standardizing with inverse law (A'A)

Similar to SOP standardization, here we do the same. But instead of `D' + D` we use `D'D` to get the variable to the terms

![](../../../assets/Images%201/Pasted%20image%2020221008125301.png)

# Simplifies logic expressions using Karnaugh map

![](../../../assets/Images%201/Pasted%20image%2020221008131702.png)

Let's take a 2 bit example
1. Find the no of cells (`2**2 = 4`) 
2. Add the gray code to the table cols and rows (here only in cols since 4 cols )

```
This is the gray code you need to remember

00
01
11
10
```


Here a 0 is an input with bar (`'`) since the input is in the format of `AB` in hte left up cell, `00` means `A'B'` , `01` means `A'B` 

![](../../../assets/Images%201/Pasted%20image%2020221008131641.png)


3. Then we cross-reference the terms we see in our SOP expression, I.e `A'B'C` we put a 1 (since its a SOP expression and it's made my min terms) in the cell under `A'B'` and `C` which is the 2nd row in 1st col

We put zeros to the remaining cells


![](../../../assets/Images%201/Pasted%20image%2020221008132058.png)

4. Then we group the cells with of 1 with multiples of 2 or 1(1,2,4,8). There are some rules when grouping them

![](../../../assets/Images%201/Pasted%20image%2020221008133218.png)

![](../../../assets/Images%201/Pasted%20image%2020221008133230.png)

![](../../../assets/Images%201/Pasted%20image%2020221008133243.png)

![](../../../assets/Images%201/Pasted%20image%2020221008134000.png)


5. Once we have the table filled up and grouped, we need to look for non-changing variables through the cols and rows to the group. I.e 3rd col has two 1s.

![](../../../assets/Images%201/Pasted%20image%2020221008134648.png)

And the `AB` value of the 3rd col in same to the 1 in the first row and the 2nd row. So that means it doesn't change. So we pick `AB` And then we go for the row, looking at the 1st row it's a `C` and in the 2ns row it's a `C'` So we can't pick that

![](../../../assets/Images%201/Pasted%20image%2020221008135030.png)

In the 1st and the 4th col the value of A changes. Because in the 1st col its `A'` but its the 4th col its `A` But `B'` is same in both. So we pick  `B`
![](../../../assets/Images%201/Pasted%20image%2020221008134927.png)

Then we look for the row, in the 2nd row it's `C`. And since both the 1s are in the 2nd row, the `C` value doesn't change for them. So we pick `C` too

Now in the end we get our picked values and form the expression. Since this was a SOP, we separate these with a `+`

```
z = AB + B'C
```

- **With SOP, we grouped the cells with `1`. So when it comes to getting POS, we just group the cells with `0`** All the other steps are the same

- In a given question, normally when we fill the map, usually we use the SOP 



