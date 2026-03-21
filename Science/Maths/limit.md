#calculus #maths #derivatives 
Suppose _f(x)_ is defined when _x_ is near the number _a_. (This means that _f_ is defined on some open interval that contains _a_, except possibly at _a_ itself.) Then we write: $$\lim_{x \to a} f(x) = L$$ and say "the limit of _f(x)_, as _x_ approaches _a_, equals _L_"

1. if we can make the values of _f(x)_ arbitrarily close to _L_ (as close to _L_ as we like) by taking _x_ to be sufficiently close to _a_ (on either side of _a_) but note equal to _a_.

2. if for every number $\varepsilon > 0$ there is a number $\delta > 0$ such that
$$\text{if } 0 < |x - a| < \delta \quad \text{then} \quad |f(x) - L| < \varepsilon$$

**One-Sided Limits**: $\lim_{t \to 0^-} H(t) = \text{a} \quad \text{and} \quad \lim_{t \to 0^+} H(t) = \text{a}$ 

=> $\lim_{x \to a} f(x) = L$ if and only if $\lim_{t \to 0^-} H(t) = L$ and $\lim_{t \to 0^+} H(t) = L$ 

## Calculating Limits Using the Limit Laws
1. $\lim_{x \to a} [f(x) + g(x)] = \lim_{x \to a} f(x) + \lim_{x \to a} g(x)$
2. $\lim_{x \to a} [f(x) - g(x)] = \lim_{x \to a} f(x) - \lim_{x \to a} g(x)$
3. $\lim_{x \to a} [c f(x)] = c \lim_{x \to a} f(x)$
4. $\lim_{x \to a} [f(x) g(x)] = \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x)$
5. $\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)} \text{ if } \lim_{x \to a} g(x) \neq 0$
6. $\lim_{x \to a} [f(x)]^n = [\lim_{x \to a} f(x)]^n$ where _n_ is a positive integer
7.  $\lim_{x \to a} c = c$
8.  $\lim_{x \to a} x = a$
9.  $\lim_{x \to a} x^n = a^n$
10. $\lim_{x \to a} \sqrt[n]{x} = \sqrt[n]{a}$
11. $\lim_{x \to a} \sqrt[n]{f(x)} = \sqrt[n]{\lim_{x \to a} f(x)}$ where n is a positive integer. (If n is even, we assume that $\lim_{x \to a} f(x) > 0$
12. If $f$ is a polynomial or a rational [[function]] and $a$ is in the domain of $f$, then $\lim_{x \to a} f(x) = f(a)$
13. If $f(x)$ = $g(x)$ when $x$ $\neq$ $a$, then  $\lim_{x \to a} = \lim_{x \to a} g(x)$, provided the limits exist
14. $$\text{If } f(x) \leqslant g(x) \text{ when } x \to a, \lim_{x \to a} f(x) \leqslant \lim_{x \to a} g(x)$$
15. $$\text{If } f(x) \leqslant g(x) \leqslant h(x) \text{ and } \lim_{x \to a} f(x) = \lim_{x \to a} h(x) = L$$
$$\lim_{x \to a} g(x) = L$$