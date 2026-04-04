#calculus #maths #principles 
> A [[function]] is continuous on an interval if it is continuous at every number in the interval. (If $f$ is defined only on one side of an endpoint of the interval, we understand continuous at the end point to mean continuous from the right or continuous from the left.

A [[function]] $f$ is **continuous** at a number $a$ if $\lim_{x \to a} f(x) = f(a)$. 
- From the right: $\lim_{x \to a^+} f(x) = f(a)$
- From the left: $\lim_{x \to a^-} f(x) = f(a)$

---
# Theorem
1. If $f$ and $g$ are continuous at $a$ and $c$ is constant, then the following functions are also continuous at $a$: $f + g$; $f - g$; $cf$; $fg$; $f / g$
2. Any polynomial is continuous everywhere; that is, it is continuous on $R$
3. Any rational function is continuous wherever it is defined; that is, it is continuous on its domain.
4. The following types of functions are continuous at every number in their domains: polynomials, rational functions; root functions; trigonometric funtions
5. If $f$ is continuous at $b$ and $\lim_{x \to a} g(x) = b$, then $\lim_{x \to a} f(g(x)) = f(b)$. In other words:
$$\lim_{x \to a} f(g(x)) = f\left(\lim_{x \to a} g(x)\right)$$
6. If $g$ is continuous at $a$ and $f$ is continuous at $g(a)$, then the composite function $f \circ g$ given by $(f \circ g)(x) = f(g(x))$ is continuous at $a$