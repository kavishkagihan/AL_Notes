<iframe width="760" height="515" src="https://www.youtube.com/embed/AMj0xyJ832E?si=OXMhr7TDf-VAyR6H" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

- Setup

![](../../assets/Images/Pasted%20image%2020240812201829.png)

First we need to use the meter bridge and measure the initial resistance of the copper coil. Then we increase the temperature of the water beaker little by little and then get the reading of the resistance.

![](../../assets/Images/Pasted%20image%2020240812202420.png)

Using the meter bridge relation, we can build up an equation for this.

$$
\begin{align*}
R_o &= Initial\ Resistance\ of\ the\ Coil\\ 
R &= Resistance\ of\ the\ Coil \\
r &= Known\ Resistance\\
\alpha &= temperature\ coefficient\ of\ resistance\\
\\
\frac{R}{r} &= \frac{l}{100 -l}\\ 
Using\ R = R_o(1 _ \alpha \theta)\\ 
\frac{R_o(1 + \alpha \theta)}{r} &= \frac{l}{100 -l}\\
\\
\therefore \frac{l}{100 -l} &= \frac{R_o\alpha}{r}\theta + \frac{R_o}{r} \\
y &= mx + c
\end{align*}
$$

![](../../assets/Images/Pasted%20image%2020240812235114.png)

Here we can find $\alpha$ using the gradient of this graph

$$
\begin{align*}
Gradient &= m = \frac{R_o \alpha}{r}\\
Intercept &= c = \frac{R_o}{r}\\
\therefore \alpha &= \frac{m r}{R_0} = \frac{m}{c} = \frac{Gradient}{Internept}
\end{align*}
$$
# Important points

> All the important points mentioned in the previous meter bridge practical applies to here as well [32A - Determination of an unknown resistance using Meter Bridge](32A%20-%20Determination%20of%20an%20unknown%20resistance%20using%20Meter%20Bridge.md)

- Why do we put the copper coil inside a water beaker?
```
To measure the temperature of the coil efficiently
```

- What is the use of the stirrer here?
```
To make sure the temperature of uniform throughout the water beaker
```

- We should keep a wire mesh at the bottom of the beaker when we heat it. Why?
```
To make sure we are giving the heat uniformly to the beaker.
```

![](../../assets/Images/Pasted%20image%2020240812203514.png)

- Why it's best to use an accumulator in this experiment instead of a dry cell?
```
We need to ensure the same amount of voltage is supplied throughout this experiment. With a dry cell the voltage could decrease after using for a while. So its best to use an accumilator for this experiment.

(But after getting a reading make sure to turn off the supply otherwise the meter bridge wire might get heated up and expand)
```