# Proof of algebraic theorem of limits

$$
\lim_{x \to a} \frac{(x^n - a^n)}{x -a} = an^{n-1}
$$

- Consider $$\frac{(x^n - a^n)}{x -a}$$
- As the degree of the denominator is `n` the number of terms it should have is `n+1`. 

> [!Example]
> $$(x + 1)^2 = x^2 + 2x + 1$$
> 
> Here when `(x + 1)^2`  (degree,n =2 )is expanded there are 3 terms `(n+1)`
> 
> $$degree + 1 = No.\ of\ terms$$

- Also, the degree of the quotient `Q(x)` when the denominator is divided by the numerator should be `n-1`


> [!Example]
>  $$\frac{x^2 + 2x  + 1}{x+1} = x+1$$
> Here when `x^2 + 2x + 1` of degree 2 (n = 2) is divided by `x + 1` of degree 1, the quotient `Q(x)` is `x + 1` which is of degree 1 `(n-1)`
> 
> $$Degree\ of\ Q(x) + Degree\ of\ numerator = No.\ of\ terms$$


- Which also means the `Q(x)` should have `n` (`(n-1) + 1`) number of terms.
- But when dividing these, we only have the first and the last term of the normal expansion. So we need to fill in the others according to the general format of expansion.

> [!Example]
> 
> $$ (a + b)^3 = a^3b^0 + 3a^2b^1 + 3a^1b^2 + a^0b^3$$

- Here, we need the coefficient of the additional terms as 0

$$
x^n - a^n = a^0x^n + 0.a^{1}x^{n-1} + 0.a^{2}x^{n-2} + 0.a^{3}x^{n-3} + .....  - a^nx^0
$$

- Now using the long division we can divide these and get a `Q(x)` as follows


$$
\frac{(a^0x^n + 0.a^{1}x^{n-1} + 0.a^{2}x^{n-2} + 0.a^{3}x^{n-3} + ...  - a^nx^0)}{x -a} = a^{0}x^{n-1} + a^{1}x^{n-2} + a^{2}x^{n-3} + ... + a^{n-1}x^{0} 
$$

- Then we take the limit of both side for `x` reaches to `a`

$$
\lim_{x \to a} \frac{(x^n - a^n)}{x -a} = \lim_{x \to a} a^{0}x^{n-1} + a^{1}x^{n-2} + a^{2}x^{n-3} + ... + a^{n-1}x^{0} 

$$
- Simplify RHS by substituting `a` to `x` as it reaches `a`

$$
\lim_{x \to a} \frac{(x^n - a^n)}{x -a} = a^{0}a^{n-1} + a^{1}a^{n-2} + a^{2}a^{n-3} + ... + a^{n-1}a^{0}

$$

- Then simplify the indices
$$
\lim_{x \to a} \frac{(x^n - a^n)}{x -a} = a^{n-1} + a^{n-1} + a^{n-1} + .... + a^{n-1}
$$


> Here we can see the $a^{n-1}$ term is recurring.
> 
- Since we know the `Q(x)` should have `n` number of terms, we can rewrite this as follows.

$$
\lim_{x \to a} \frac{(x^n - a^n)}{x -a} = na^{n-1}
$$