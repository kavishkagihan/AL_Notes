---
tags:
  - HydroStatics
---

<iframe width="760" height="515" src="https://www.youtube.com/embed/rrtu-DAk5aw?si=V75_EiiEmawe4wFT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Method 1 - Using the density bottle - Not in the syllabus

When using the **density bottle**, we can't get the densities of the liquids to find the relative density. Instead, we use their masses.

> Here, we need to make sure the same volumes of both liquids are used. Why?,

We know that,

$$
Relative\ Density = \frac{Density\ of\ the\ liquid}{Density\ of\ water}
$$


We multiply both numerator and denominator with `V`, the **volume**. Since `density * volume = mass` we can derive the following equation

$$
Relative\ Density = \frac{Mass\ of\ liquid\ of\ volume\ v}{Mass\ of\ water\ of\ volume\ v}
$$


- Initial setup

There are a couple of readings that you need to get before doing the calculation

- `m1` -> Mass of the empty bottle `b`
- `m2` -> Mass of the bottle + water fully filled up to the top (of volume `V`)
- `m3` -> Mass of the bottle + the liquid (Oil) filled up to the top 
- `m4` -> Mass of the bottle + sand filled up to a certain level (of volume `Vo`) 
- `m5` -> Mass of the bottle + sand filled up to the same level as `m4` reading (of volume `Vo`) + water to fill the rest of the bottle to the top (of volume `V - Vo`)

>`m1`, `m2` and `m3` are enough to get the relative density of a liquid, but to get the relative density of any other substance, we need to get an additional reading of `m5`
![](/assets/Images/Pasted%20image%2020230829142837.png)

- The **relative density of the liquid** (Oil) can be written as,

$$
Relative\ Density = \frac{m3 - m1}{m2 -m 1}
$$



- To get the relative density of sand, we need 2 main readings

$$
\begin{align*}
Mass\ of\ sand\ (of\ Volume\ Vo) & = m4 -m 1 \\
Mass\ of\ water\ (of\ Volume\ Vo) &=  (m2 - m1) - (m5 - m4) \\
&=  ((b + V) - b ) - ( (b + Vo + (V - Vo)) - (b + Vo) ) \\
&= (V0) - (V + Vo) \\
&= Vo
\end{align*}
$$

Therefore, the **relative density of the substance** (sand) can be written as,




$$Relative\ density = \frac{m4 - m1}{(m2 - m1) - (m5 - m4)}$$

> When the bottle is filled with sand, it doesn't fill the whole bottle's volume
- What is the reason we need to get an additional reading when getting the relative density of a solid substance like sand?
```
When we fill the bottle with sand, its not going to fill the total volume of the bottle with sand. Reason being, as sand particle have spaces in between them, there is going to be some space left unfilled. Therefore we add some volume of water and use an addition reading to get the volume of that water and then the volume of sand. 
```

> Thickness of the density bottle at top is high compared to the lower part
- Once we have filled the bottle with a liquid, why should we hold it from the top instead of from the bottom?

```
In the bottom part the thickness of the glass is less, compared to the top. And since our body temperature is greater compared to the environment, if we hold it from the bottom heat would get transfered to the liquid and it could expand
```

> If you don't have a density bottle, you can use a beaker to find the masses.
- What is the other method that you can use if you don't have a density bottle for this experiment.

```
You can use a beaker and a tripple beam balance to find the masses of the liquids
```

>First you fill the beaker with the liquid (oil in our case), get its mass -> `Ml`. Then remove the oil, fill in with water and get the mass -> `Mw`.
- In here as well, we need to use the same volume of both liquids
- Then the $Relative\ density = \frac{M1}{Mw}$

> But this method has a **certain error** when using the beaker **with wide opening**.

- What is the error we get from this method?

```
When we fill the beaker with the liquid and water, the top liquid surface is not going to be flat. It's going to create a meniscus (due to surface tension). The level of this meniscus depends on the nature of the liquid. And since water and the liquid we use are different, the level of the meniscus aren't going to be the same. Therefore, the volume we measure for both the liquid are not going to be the same.
```

![](/assets/Images/Pasted%20image%2020230829132759.png)

>This error can be minimized by using a **tube with a smaller opening**, like a capillary tube

- How can we minimize this error?

```
By using a capilary tube with a much smaller opening than a beaker (When we take a narrow tube, the curvature's difference is very small. Therefore, we can ignore it)
```

## Method 2 - Using a weighted boiling tube

 ![](../../assets/Images/Pasted%20image%2020230901161805.png)

> To sink the test tube, lead shots are placed at the bottom of the test tube and sealed with wax

- What are the 2 main advantages of sealing the bottom part of the test tube with lead shots and wax?

```
We can keep the test tube vertical inside the water beaker

We can ignore the irregular part of the test tube when taking it's inside volume
```

![](../../assets/Images/Pasted%20image%2020230901162030.png)

(we can't find the volume of the irregular part as there is no exact cross-sectional area)

> The scale should start from the end of the wax layer
- How do we fix the scale to the test tube?
```
Take a graph paper and mark the scale accordingly. Take a print and paste it in the inside of the test tube so that it wont get contacted with the liquid on the outside the test tube.
```

- Setup
![](../../assets/Images/Pasted%20image%2020230901164529.png)

![](/assets/Images/Pasted%20image%2020230901164606.png)

> Here the external diameter should be taken  when getting the A

- Why should we take the external diameter when getting the cross-sectional area of the test tube to find the volume?
```
Because we are getting the volume for the water displaced by the test tube. For that the external cross sectional area should be used. So we need to get the external diameter
```

- How do we get the external diameter of the test tube?
```
Use a vernier caliper and get 2 reading of the external diameter which are perpendicular. Take at least 2 such points and get the 2 readings for them. Then take the average value as the diameter to calculate the cross sectional area. 
```

> The theory we use here is the Archimedes principle, which is `u = mg` (Weight of the test tube is equals to the upthrust as it floats)

$$
\begin{align*}
u &= mg \\ 
v\rho g &= mg \\
(V + Al)p &= (M+m) \\
% Subject the l term
V + Al &= \frac{(M+m)}{\rho} \\
l &= \frac{(M+m)}{\rho A} -\frac{V}{A} \\
% Format it accordingly
l &= \frac{1}{\rho A}m + \frac{1}{A}(\frac{M}{\rho} - V) \\
l &= \frac{1}{\rho A}m + \frac{1}{A \rho}(M - V\rho)
\end{align*}
$$
> Here we need to subject `l` as it should be the `y` axis and format it later so that it fits the $y = mx + c$ format

(`m` is the x-axis as we change the known masses by adding weights to the test tube)

> So the density can be calculated using the gradient of the graph

$$
\begin{align*}
	Gradeint &= \frac{1}{\rho A} \\ 
	\rho &= \frac{1}{ Gradient . A}
\end{align*}
$$



