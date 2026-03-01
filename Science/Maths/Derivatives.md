# Rates of Changes
- The **tangents line** to the curve $y = f(x)$ at the point $P(a, f(a))$ is the line through $P$ with the slope $$m = \lim_{x \to a}\frac{f(x) - f(a)}{x - a} = \lim_{h \to 0}\frac{f(a + h) - f(a)}{h}$$ provided that this limit exists

- The **derivative of a function $f$ at a number $a$**, denoted by $f'(a)$, is $$f'(a) = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h} = \lim_{x \to a}\frac{f(x) - f(a)}{x - a}$$


> [!NOTE] Note
> The tangent line to $y = f(x)$ at $a$ is the line through $(a, f(a))$ whose slope is equal to $f'(a)$, the derivative of $f$ at  $a$.
> The derivative $f'(a)$ is the instantaneous rate of change of $y = f(x)$ with respect to $x$ when $x = a$.

# The Derivative as a Function
- $f'$ is the **derivative of $f$** and defined by:  $$f'(x) = \lim_{h \to 0} \frac{f(x + h) - f(x)}{h}$$

- A function $f$ is **differentiable at $a$** if $f'(a)$ exists. It is **differentiable on an open interval** $(a, b)$ [or $(a, \infty)$ or $(-\infty, a)$ or (-\infty, \infty)] if it is differentiable at every number in the interval

> [!NOTE] Note
> If $f$ is differentiable at $a$, then is [[Functions and Limits#Continuity|continuous]] at $a$.

- **Higer Derivatives**: $$\frac{d}{dx}(\frac{dy}{dx})=\frac{d^2y}{dx^2}$$

## Differentiation Formulas
1. $\frac{d}{dx}(c) = 0$
2. The Constant Multiple Rule: If $c$ is a constant and $f$ is a differentiable function, then: $$\frac{d}{dx}[cf(x)] = c\frac{d}{dx}f(x)$$
3. The Sum Rule: If $f$ and $g$ are both differentiable, then $$\frac{d}{dx}[f(x) + g(x)]= \frac{d}{dx}f(x) + \frac{d}{dx}g(x)$$
4. The Difference Rule: If $f$ and $g$ are both differentiable, then $$\frac{d}{dx}[f(x) - g(x)]= \frac{d}{dx}f(x) - \frac{d}{dx}g(x)$$
5. The Product Rule: If $f$ and $g$ are both differentiable, then $$\frac{d}{dx}[f(x)g(x)]= g(x)\frac{d}{dx}f(x) + f(x)\frac{d}{dx}g(x)$$
6. The Quotient Rule: If $f$ and $g$ are differentiable, then $$\frac{d}{dx}[\frac{f(x)}{g(x)}] = \frac{g(x)\frac{d}{dx}f(x) - f(x)\frac{d}{dx}g(x)}{[g(x)]^2}$$
7. General Power Functions: If $n$ is a positive integer, then $$\frac{d}{dx}(x^{-n})=-nx^{-n-1}$$
8. The Power Rule (General Version): If $n$ is any real number, then $$\frac{d}{dx}(x^n) = nx^{n-1}$$

==Derivatives of Trigonometric Functions==
