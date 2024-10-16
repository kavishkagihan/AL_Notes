# Proof of $\int_{b}^{a} f(x).dx = \int_{b}^{a} f(a + b - x).dx$

1. First, use a substitution and change the domain of f(x)

$$
\begin{align*}
\int_{b}^{a} f(x).dx\  and& \int_{b}^{a} f(a + b - x).dx
\\ \\
let\ t =& (a +b - x) \\
x=& (a +b -t)
\\
f(x) \to& f(a +b - t) \\\\
\therefore \int_{b}^{a} f(x).dx =& \int_{b}^{a} f(a + b - t).dx
\end{align*}
$$

2. Differentiate the substitution with respect to x.


$$
\begin{align*}
t =& (a + b -x) \\
\frac{dt}{dx} =& (-1) 
\end{align*}
$$

3. Change the d-operator in the integral

$$
\begin{align*}
& \int_{b}^{a} f(a + b - t).dx \\
&\int_{b}^{a} f(a + b - t). (-1)dt \\
& -\int_{b}^{a} f(a + b - t).dt
\end{align*}
$$


> [!Example]
> Here we can interchange the limit as there is a negative sign (`-`) in the front of the integral
>
$$-\int_{b}^{a} g(x).dt = \int_{a}^{b} g(x).dt$$

$$
\begin{align*}
-\int_{b}^{a} f(a + b - t).dt =&  \int_{a}^{b} f(a + b - t).dt
\end{align*}
$$

4. Change the limit according to the new substitution.

$$
\begin{align*}
\int_{x=a}^{x=b} f(a + b - t).dt \\
t = a + b - x\\
\\
x = a \to t =& a + b - a \\
t =& b
\\\\
x = b \to t =& a + b - b \\
t =& a
\\\\
\therefore \int_{t=b}^{t=a} f(a + b - t).dt
\end{align*}
$$

5. Finally, we can look at the format and come to the conclusion


$$
\begin{align*}
as\ t\ and\ x\ are\ both\ variables, t \to x \\ \\
\therefore \int_{b}^{a} f(a + b - t).dt =  \int_{b}^{a} f(a + b - x).dx
\end{align*}
$$






