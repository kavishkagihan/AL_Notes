
# Number systems

- Computer doesn't understand 0,1 it understands the presence and absence of current
- Presence of current - 1, absence of current - 0
- Voltage from 0v - 0.8v -> 0 and 2v - 5v ->1
- 0.8v – 2.0v –>uncertain area

![](../../../assets/Images%201/Pasted%20image%2020220907102009.png)

- **American National Standard Institute** proposed (ANSI) to use ASCII
- This was proposed in order for all to use the same standard when representing characters (Requirement of a character set)
- Character set is a standard way to represent characters.
- There are a couple of character representation methods
	- BCD (Binary Coded Decimal)
	- EBCDIC (Extended Binary Coded Decimal Interchange Code)
	- ASCII (American Standard Code for Information Interchange)
	- Unicode

### BCD
- **4 bit** representation (`2**4 = 16`)
- total number of characters that can be represented - **16** (`2**4 = 16`)
- used to represent numbers (0-9) 
	- 1 -> 0001 | 8 -> 1000
- But for digits with two numbers 8 bits are used.
	- 10 -> 0001 0000 | 12 -> 0001 0010

### ASCII
- 8 bit representation, However, the last bit (first one from left) is used as the **check digit**, so the representable bits are **7**
- This last bit is used to check the type of the entered character (whether it's a number, special character, function key or a letter etc.)
- total number of characters that can be represented - **128** (`2**7 = 128`)
- Originally proposed by ANSI
- **IBM personal computers** use ASCII


### EBCDIC 
- typically used by **IBM mainframe computers**
- **8 bit** representation 
- total number of characters that can be represented - **256** (`2**8 = 256`)

### Unicode
- 16 bit representation
-  total number of characters that can be represented - **65536** (`2**16 = 65536`)


![](../../../assets/Images%201/Pasted%20image%2020220907103618.png)
![](../../../assets/Images%201/Pasted%20image%2020220907103630.png)

## Data Representation
There is a special system to represent characters with ASCII

- Representation of characters
If we press A, the `A` gets the ASCII value for it which is `65` Then it's its converted to binary which is `1000001` and sent to  interpret.

`A` -> `65` -> `1000001`

![](../../../assets/Images%201/Pasted%20image%2020220903121346.png)

- Representation of Images

First the image is divided into rows and columns and a **bitmap** is made. If 2 colors are used to represent the image (I.e black and white images) black is represented by 1 and white is represented by 0.

Since there are 2 colors only 1 bit is needed `2**1 = 2`

1 -> black
0 -> white

| 1   | 0   | 1   | 1   |
| --- | --- | --- | --- |
| 0    |1     |1     |1     |
| 1   | 0   | 1   | 1   |
| 0    |1     |1     |1     |

![](../../../assets/Images%201/Pasted%20image%2020220903121424.png)

If we need to represent 4 colors, 2 bits are needed `2**2=4`

00 -> white
11 -> black
01 -> red
10 -> blue

| 01  | 11  | 00  | 11  |
| --- | --- | --- | --- |
| 01  | 11  | 00  | 11  |
| 11  | 01  | 00  | 10  |
| 01  | 11  | 00  | 11  |

- Representation of Videos

Videos are separated into frames, and then made together with a specific frame size (fps) These frames are represented just like images

- Representation of Audios

Audio is a continues analog signal. Computers can't understand analog signals. So the analog signals are covered to digital signals.


We cannot digitize all the analog values into Digital values. Because Analog signal has an infinite number of values. So, we take sample values then digitize them.

![](../../../assets/Images%201/Pasted%20image%2020220903122152.png)

### Conversion between fractional numbers

#### Fractions to binary

- Multiply the given decimal fraction by 2. 
	- It's multiplied by 2 because its binary, if octal multiply by 8,if hexadecimal by 16
- Multiply by 2 until the decimal part becomes 0.
- Write the values in front of decimal point from top to bottom.

![](../../../assets/Images%201/Pasted%20image%2020220903123942.png)

```
0.3125 --> 0.0101
0.625 --> 0.101
0.25 --> 0.01
0.50 --> 0.1
```

![](../../../assets/Images%201/Pasted%20image%2020220903123932.png)

Same theory goes for octal and hex

- Octal

![](../../../assets/Images%201/Pasted%20image%2020220903124339.png)


