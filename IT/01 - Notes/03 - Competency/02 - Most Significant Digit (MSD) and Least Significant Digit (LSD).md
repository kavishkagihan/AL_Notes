
# Most Significant Digit (MSD) and Least Significant Digit (LSD)


- **MSD - The Digit that contain the most positional value in a number.** 
- **LSD - The Digit that contains the least positional value in a number.**

![](../../../assets/Images%201/Pasted%20image%2020220903124702.png)

With binary or octal or hex, you need to get the position of the MSB and LSB and then raise to power of the position

100100 
	-> MSB = `2**6` (1 in the left-hand side in the 6th position)
	-> LSB = `2**0` (0 in the right-hand side in the 0th position)

Here, 0 is considered because if another 0 is added in the end, the value of the number changes. But with decimal numbers (32.41) this doesn't matter. Even if we add another 0 at the end, the value **doesn't change**

Octal and hexadecimal number systems are there for **human convenience**. This helps to compress data and make it short so that's easy to read and interpret. 


## Signed Integers

To **represent negative numbers, these signed integers are used**. There are 3 ways to do this.
1. Signed Magnitude Representation
2.  1’s Complement
3. 2’s Complement


#### Signed Magnitude Representation

The left most bit is used as the singed bit

![](../../../assets/Images%201/Pasted%20image%2020220903130345.png)

Here the 0 is left last bit tells that the number is a positive number. If it's 1 its a negative

0 -> positive
1 -> negative

The conventional bit length is 8 (ASCII format)

![](../../../assets/Images%201/Pasted%20image%2020220903130515.png)

If its a 4 bit computer, we can have 16 possibilities, But here we don't represent numbers from 0-15. Here 7 bits are given for positive numbers and 7 bits for negative. And other 2 numbers are for 2 zeros.

![](../../../assets/Images%201/Pasted%20image%2020220903130941.png)

##### Problems of sign magnitude
- One problem in this is that **it has 2 zeros**. A +0 (0000) and a -0 (1000) This is mathematically wrong.

- **Subtraction (other calculations too) of negative values can't be done**. The computer can't do other calculations other than addition (that's why its called adding machine). Every other calculation like -, * and % is done by addition

![](../../../assets/Images%201/Pasted%20image%2020220903131305.png)

A problem arises when we try to add a positive number to a negative number

![](../../../assets/Images%201/Pasted%20image%2020220903131419.png)

-3 + 3 should be 0 but here it's giving -6

### 1’s Complement

This affects to negative numbers. Here we flip the numbers for the negative numbers
For a 1 we use 0 and for a 0 we use 1

1011 is -3, since its a negative we do a 1's Complement  to the positive of it (3). Even though we are doing the 1's compliment to the -3 we do the flip to the positive value of the digit which in this case is 3. (if we wanted to do 1's compliment to -5 we use 5 (0101) and then flip it `0101 -> 1010`)

```txt
3 = 0011 -> do 1's Complement -> 1100
```

Now we do the calculation

```txt
3 + (-3) = 0011 + 1100 (this is the value for doing 1's complement for 3) 

0011 + 1100 = 0
```

- I.e 3+ (- 5) 
	1. get binary for 3 and 5
		- `3 = 0011,  5 = 0101`
	2. do 1's complement for 5 since it's a negative used.
		 - `0101 -> 1010 ; (-5) -> 1010 (not the real value for -5)`
	3. Then do the calculation
		 - ` 0011 + 1010 = 1101`

But here is `1101 = -2`? No! If  the answer is a negative, first we need to do 1's complement to the value and flip it. Then its converted to decimal

```txt
1101 -> 0010 = 2
```

- Problems with 1's compliments
	- We still have the 2 zeros problem

- The second problem we had is solved though. We now can do calculations with negative numbers

If the answer overflows the max number of bits, the overflowing bit is called the **Carry bit**. We need to add this carry bit to the answer itself (LSB of the answer - last bit ) to get the accurate answer.

![](../../../assets/Images%201/Pasted%20image%2020220907105830.png)

### 2's Complement 

This is **done to negative numbers** too. Here the same process happens like the 1's complement. The difference is we have to add 1 after the 1's complement is done.

2's complement for -3
```txt
3 = 0011 -> 1's complement -> 1100
```

Add one to the answer of 1's complement

```txt
1100 + 0001 = 1101 = -3 (This can't be reverted like 1's complement)
```

We can confirm our answer from this table

![](../../../assets/Images%201/Pasted%20image%2020220910121658.png)

+8 can't be represented with 4 bits according to this, you have to use 5 bits to represent that.

Now that we have that, if this is correct, if we add +3 to -3 it should result in 0 ryt. Let's see.

![](/IT/Images/Pasted%20image%2020220910122102.png|300)

No here one bit get's overflown. Therefore, we just discard that bit. (In 1's compliment we add it to the LSB, here we just discard it) So as the final answer, we get `0000` which is 0

Let's see another example of `4 - 6`

![](../../../assets/Images%201/Pasted%20image%2020220910122631.png)

Here we get the answer as `1110` but this is not `-2` So what we have to do to get the correct decimal value is as follows.
	1. See what the sign bit is.
	2. if its `0` (positive answer) then no problem, keep it as same and convert to decimal. 
	3. If it's `1` (negative answer), flip the bits `1110 -> 0001` and then add one to the end (LSB) `0001 + 0001 = 0010`
	4. Get the final answer as `0010` which is the binary equivalent to `2`  and if the sign bit was `0`, no problem, keep it as it is. But if it's `1` the answer is negative. (The sing checking it done to the value we get before flipping. In this case for `1110`)
	5. Since the check bit of the answer is `1`  the answer is negative which is `-2`

---
NOTE: One thing to remember here is that, we **can't subtract** values from the answer. So we **can't subtract 1 from the answer and then do the flip**. What we have to do is that first we need to **do the flip and then add 1 to the answer**

```
answer - 1 -> do the flip ------- WRONG

do the flip -> answer + 1 ------- Correct
```

Nonetherless the answer with both ways is going to be the same but the first method is wrong!

---
Here since the sign bit is `1`, the answer becomes negative which is `-2`

**Advantages of 2's compliment**
	- Operations are simpler.
	- 2 zero problem is gone.
	- In modern computers, this method is mostly used.
	- Makes it possible to build low cost, high speed hardware

![](../../../assets/Images%201/Pasted%20image%2020220910124242.png)


##### Maximum and Minimum values of these encodings (in 8 bit representation)

| Encoding       | Min  | Max |
| -------------- | ---- | --- |
| 1's Complement | 0 | 127 |
| 2's Complement | 0| 128 | 
