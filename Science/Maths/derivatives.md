#calculus #derivatives #maths 
# The Derivative as a [[function]]
- $f'$ is the **derivative of $f$** and defined by:  $$f'(x) = \lim_{h \to 0} \frac{f(x + h) - f(x)}{h}$$

- A [[function]] $f$ is **differentiable at $a$** if $f'(a)$ exists. It is **differentiable on an open interval** $(a, b)$ [or $(a, \infty)$ or $(-\infty, a)$ or $(-\infty, \infty)$] if it is differentiable at every number in the interval

> [!NOTE] Note
> If $f$ is differentiable at $a$, then is [[Mathematical Models#Continuity|continuous]] at $a$.

- **Higher Derivatives**: $$\frac{d}{dx}(\frac{dy}{dx})=\frac{d^2y}{dx^2}$$

## Differentiation Formulas
1. $\frac{d}{dx}(c) = 0$
2. The Constant Multiple Rule: If $c$ is a constant and $f$ is a differentiable [[function]], then: $$\frac{d}{dx}[cf(x)] = c\frac{d}{dx}f(x)$$
3. The Sum Rule: If $f$ and $g$ are both differentiable, then $$\frac{d}{dx}[f(x) + g(x)]= \frac{d}{dx}f(x) + \frac{d}{dx}g(x)$$
4. The Difference Rule: If $f$ and $g$ are both differentiable, then $$\frac{d}{dx}[f(x) - g(x)]= \frac{d}{dx}f(x) - \frac{d}{dx}g(x)$$
5. The Product Rule: If $f$ and $g$ are both differentiable, then $$\frac{d}{dx}[f(x)g(x)]= g(x)\frac{d}{dx}f(x) + f(x)\frac{d}{dx}g(x)$$
6. The Quotient Rule: If $f$ and $g$ are differentiable, then $$\frac{d}{dx}[\frac{f(x)}{g(x)}] = \frac{g(x)\frac{d}{dx}f(x) - f(x)\frac{d}{dx}g(x)}{[g(x)]^2}$$
7. General Power Functions: If $n$ is a positive integer, then $$\frac{d}{dx}(x^{-n})=-nx^{-n-1}$$
8. The Power Rule (General Version): If $n$ is any real number, then $$\frac{d}{dx}(x^n) = nx^{n-1}$$

# Derivatives of Trigonometric Functions
1. $\lim_{h \to 0} \sin x = \sin x$; $\lim_{h \to 0} \cos x = \cos x$
2. $\lim_{\theta \to 0} \frac{\sin \theta}{\theta} = 1$
3. $\lim_{\theta \to 0} \frac{\cos \theta - 1}{\theta} = 0$
4. $\frac{d}{dx}(\sin x) = \cos x$
5. $\frac{d}{dx} (\cos x) = -\sin x$
6. $\frac{d}{dx}(\tan x) = \sec^{2}x$
7. $\frac{d}{dx}(\csc x) = -\csc x \cot x$
8. $\frac{d}{dx}(\sec x) = \sec x \tan x$
9. $\frac{d}{dx}(\cot x) = -\csc^{2}x$
