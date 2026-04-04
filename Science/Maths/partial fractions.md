#maths #calculus #integral 
> [[integral|Integrating]] any rational [[function]] (a ratio of polynomials) by expressing it as a sum of simpler fractions

$$
f(x) = \frac{P(x)}{Q(x)} = S(x) + \frac{R(x)}{Q(x)}
$$

Try to express the proper rational [[function]] $R(x)/Q(x)$ as a sum of **partial fractions** of the form
$$
\frac{A}{(ax + b)^i} \quad \text{or} \quad \frac{Ax + B}{(ax^2 + bx +c)^i}
$$

**Case I: The denominator $Q(x)$ is a product oof distinct linear factors**
$$
Q(x) = (a_1x + b_1)...(a_kx + b_k)
$$
=> 
$$
\frac{R(x)}{Q(x)} = \frac{A_1}{a_1x + b_1} + ... + \frac{A_k}{a_kx + b_k}
$$
**CASE II: $Q(x)$ is a product of linear factors, some of which are repeated.**
Suppose the first linear factor $(a_1x+b_1)$ is repeated $r$ times
$$
\frac{A_1}{(a_1x + b_1)} + ... + \frac{A_r}{(a_1x + b_1)^r}
$$
**CASE III: $Q(x)$ contains irreducible quadratic factors, none of which is repeated.**
If $Q(x)$ has the factor $ax^2 + bx + c$, where $b^2 - 4ac <0$
$$
\frac{Ax + B}{ax^2 + bx + c}
$$
**CASE IV: Q(x) contains a repeated irreducible quadratic factor.**
If $Q(x)$ has the factor $(ax^2 + bx + c)^r$, where $b^2 - 4ac <0$
$$
\frac{A_1x+B_1}{ax^2+bx+c}+...+\frac{A_rx+B_r}{(ax^2+bx+c)^r}
$$