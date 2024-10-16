
<iframe width="760" height="515" src="https://www.youtube.com/embed/-BIOiZ1U7UQ?si=xjg4UO3wDtlYDavb" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

- Setup

![](../../assets/Images/Pasted%20image%2020240811221024.png)

Here if we want to draw a graph to find the unknown resistance, we change the known resistance and take multiple readings for the balanced length


$$
\begin{align*}
R_1 = Unknown\ resistoance\\
R_2 = Known\ resistoance\\  \\
\frac{R_1}{R_2} &= \frac{l}{100 -l}\\
\frac{R_2}{R_1} &= \frac{100 - l}{l}\\
\frac{R_2}{R_1} &= \frac{100}{l} - 1\\
\\
\therefore \frac{1}{l} &= \frac{1}{100R_1}R_2 + \frac{1}{100}\\
y &= mx +c
\end{align*}
$$

![](../../assets/Images/Pasted%20image%2020240811234111.png)

From the gradient we can find the unknown resistance

$$
\begin{align*}
Gradient = m = \frac{1}{100R_1}\\ \\
\therefore R_1 = \frac{1}{100m}
\end{align*}
$$


### End Correction

Here if we are asked to **find the end-correction** of the wires, we need to add 2 variables as `x` and `y` to the lengths of the wires and build up a simultaneous equation and solve to find `x` and `y`

![](../../assets/Images/Pasted%20image%2020240811230742.png)
$$
\begin{align*}
x \to end-&correction\ for\ R_3\ resistor\\
y \to end-&correction\ for\ R_4\ resistor\\
\frac{R_1}{R_2} &= \frac{l + x}{100 - l + y}\\
\end{align*}
$$

Then by interchanging the $R_1$ and $R_2$ and finding the balanced lengths, 2 equations need to be taken and then `x` and `y` can be separately found.



 # Important points
- In the meter bridge, why do we use wide metallic(copper) strips?

```
Because the resistance in those strips should be neglagible. By increasing the Areas, resistance is decreased.
```

-  Why do we put a resistor R (usually 5k$\ohm$) before the galvanometer?
```
To protect from high current flowing through it.
```
> This is used as the safety circuit for the galvonometer.

- Why do we have a key plug at that same point?

```
At first the key plug is disconnected and current is let to pass through the resistor. But once we have found an rough position for the balanced reading, to measure the actual current passing, the key plug is connected and current is let to pass through that with 0 resistance. 

This is called short circuiting. Its an safety setup for the galvonometer
```
![](../../assets/Images/Pasted%20image%2020240811224446.png)

- Why do we have a 2nd plug key at the top closer to the cell? (For this we can also use a tap key)
```
We need to make sure that current doesn't continously flow through the circuit. So once the balanced reading is taken the circuit should be disconnected. That plug key is used for that.
```

- Why do we have to make sure the current doesn't continuously flow through the circuit?
```
If current flows continously, it will start to heat and resistivity and properties like that will change. We don't want that to happen.
```


- Here why can't we slide the slider key through the wire? Why do we need to touch a point by point?
```
Because if you slide it on the wire it may harm the wire and change the cross sectional area causing issues with resistance.
```

- When the slider is placed at 2 ends of the wire, how will the galvanometer deflect?
```
When its placed in one side it will deflect to one side, when kept in the other end it will deflet to the other side. This denotes that some point in between there is a point where the current is 0.

This is also the way we can confirm that the circuit is working and ready to take the measurements we need.
```

![](../../assets/Images/Pasted%20image%2020240811225101.png)

- Here why should the known resistance nearly be equal to the unknown resistance?
```
So that the both resistances can be measured with same accuracy.

To select nearly equal resistances, the unknown resistance has to selected such that the balancing point comes closer to the middle (meaning the ratio will be closer to 1:1)
```

- As the known resistor, why can't we use the rheostat?
```
Because with the rheostat, we can't know the magnitude of the resistance even though the resistance can be changed. Therefore a resistor box has to be used.
```

- Why is it best to chose a resistance that will give a balance length around the mid point of the wire?

```
Because that way we can measure both the lengths with same accuracy
```