
<iframe width="760" height="515" src="https://www.youtube.com/embed/Hi__wOOGBqM?si=P4T5JM5M-fyyCxhD" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

- Setup
![](../../assets/Images/Pasted%20image%2020240603213135.png)


- Functions of different components in the setup

A - To control the internal pressure of the steam generator and keep is stable.(As at atmospheric pressure the boiling point is 100C and if pressure changes so will the boiling point) Also to prevent accidents of spilling, this tube should be considerably longer

B - To take out the steam generated. (When steam is going through this tube, few amounts will get condensed and collected in the steam trap)

C - To separate the condensed water and add just the steam, to the calorimeter. 



- Measurements you need to take in the correct order.

1. Mass of empty calorimeter + stirrer. $M_1$
2. Mass of empty calorimeter + stirrer + water. $M_2$
3. Initial temperature of the calorimeter $\theta_1$
4. Maximum temperature of the calorimeter after adding steam $\theta_2$
5. Final mass of the calorimeter + stirrer after adding steam $M_3$


> Here $\theta_2 > \theta_1$


After taking these readings, we can find the specific heat capacity of the steam using the equation $H = ML$  for the phase change of water and we use $H =ms\theta$ for the other heat exchanges

> What happens to steam is that the 100C steam is converted into 100C water and then 100C water is cooled down to $\theta_2$ water

Heat released from phase change and condensed water (100C-> $\theta_2$) is gained by the calorimeter and water ($\theta_1$->$\theta_2$)


$$
\begin{align*}
M_s =& Mass\ of\ steam\ added\ (M_3 - M_2) = Mass\ of\ water\ added\\
&(As\ the\ same\ steam\ is\ condensed\ in\ to\ water)\\
M_w =& Mass\ of\ initial\ water\ in\ calorimeter\ (M_2 - M_1)\\
M_c =& Mass\ of\ the\ calorimeter\ +\ Stirer (M_1)
\\\\
L =& Spefic\ latemt\ heat\ of\ vapourization\ of\ water\\
S_w =& Spefic\ heat\ capacity\ of\ water (4200)\\
S_c =& Spefic\ heat\ capacity\ of\ calorimeter(4000)\\
\\
H =& mS\delta\theta = ML \\
M_sL + M_sS_w(100 - \theta_2) =& M_cS_c(\theta_2 - \theta_1) + M_wS_w(\theta_2 - \theta_1)
\\ \\
\therefore L =& \frac{(M_cS_c + M_wS_w)(\theta_2 - \theta_1) -M_sS_w(100 - \theta_2) }{M_s}
\end{align*}
$$

# Important points

- Why do we have to submerge the tube "A" inside water?
```
Otherwise the steam generated would escape from tube A instead of going through tube B
```

- What happens to the water if we block the tube "B"
```
As more and more steam is generated, the steam will start to take up space inside the generator and since the tube "B" is blocked the water will be pushed up through the tube "A". So the water level will gradually increase
```
