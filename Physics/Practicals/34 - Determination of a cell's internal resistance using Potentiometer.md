
<iframe width="760" height="515" src="https://www.youtube.com/embed/zMoUjNybz54?si=w00zZ--z-wgu3-7X" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

- Setup

![](../../assets/Images/Pasted%20image%2020240813194135.png)

Here once the deflection of the galvanometer is 0, the potentials are equal in the potentiometer wire and the external circuit cell.
So we can build up an equation like this.

$$
\begin{align*}
k &= potential\ greadient\ of\ potentiometer\ cell\\
l &= balance\ length\\\\
V_p &= kl \to For\ potentiometer\\
V_e &=  E - Ir \to For\ external\ cell\\
\\ E - Ir &= kl - (1)\\\\
For\ the\ external\ circuit, (KVL)\\
\Sigma E &= \Sigma IR \\
E &= IR + Ir\\
\therefore I &= \frac{E}{R+r} -(2)\\\\
Using\ (2)\ in\ (1),\\
E - (\frac{E}{R+r})r &= kl \\
\frac{ER}{R+r} &= kl \\
\frac{R + r}{ER} &= \frac{1}{kl}\\
\frac{1}{E} + \frac{r}{ER} &= \frac{1}{kl}\\ \\
\therefore \frac{1}{l} &= (\frac{kr}{E})\frac{1}{R} + \frac{k}{E}\\
y &= mx + c\\
\end{align*}
$$
![](../../assets/Images/Pasted%20image%2020240813200556.png)

Using the gradient and intercept of this graph we can find the internal resistance of the cell.

$$
\begin{align*}
Gradient &= m = \frac{kr}{E}\\
Intercept &= c = \frac{k}{E}\\
\\
\therefore r &= \frac{m}{c} = \frac{Gradient}{Intercept}
\end{align*}
$$
# Important Points

All the important points regarding the potentiometer in [Important Points](33%20-%20Comparing%20the%20EMF%20of%20two%20cells%20using%20Potentiometer#Important%20Points) are applied here.

- In this experiment, 2 balance lengths should be taken. What are those?
```
With the switch (in the external circuit) open and with the switch closed
```

$$
\begin{align*}
l_1 \to With\ switch\ open\\
l_2 \to With\ switch\ closed\\\\
E &= l_1k\\
E -Ir &= l_2k
\end{align*}
$$
> Using this also you can find the internal resistance instead of going for a graphical method.

- What would the reason for E (EMF) to be constant even after changing the resistance of the resistance box?
```
The infinity key in the resistance box could be removed.

Usually when the a key is unplugged or plugged in the resistance box, resistance changes and therefore current flowing changes, resulting in changing of potential difference. But if the infinity key is unplugged in the resistor box, no matter which other key is plugged or not the resistance is going to be infinity and the potential difference will stay a constant value.
```

  - In this case, should the EMF of the accumulator always be greater than the EMF of the external cell? And why?
```
It doesn't have to be a bigger. It can even be equal. Because in this case the effective potential of the external cell is (E - Ir), not E. Therefore, even if 2 potentials of the cells were equal, still there will be difference for us to balance from the potentiometer cable. So here for this to be possible the condition that needs to be satisfied is E - IR < E_p (Accumilator cell)

This is not the case in previous experiments. Thats becuase we assumed that the internal resistance of the external cell was negligible in those cases. But not here.
```

- In this experiment, near the accumulator why can't we use a tap key instead of a plug key?
```
Because we need to keep the connection connected a little while for the potential to be stabalized. With a tap key the connection is connected and disconnected within a few seconds. So for that reason its best to use a plug key in this case.
```