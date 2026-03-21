#calculus #maths #integral
If $f$ is a [[function]] defined for $a \leqslant x \leqslant b$, we divide the interval $[a, b]$ into $n$ subintervals of equal width $\Delta x = (b - a) / n$. We let $x_0 (= a)$, $x_1,..., x_n (= b)$ be the endpoints of these subintervals and we let $x^*_1,...,x^*_n$ be any **sample points** in these subintervals, so $x^*_i$ lies in the $i$th subinterval $[x_{i-1}, x_i]$. Then the **definite integral of $f$ from $a$ to $b$** is $$\displaystyle \int_{a}^{b} f(x)dx = lim_{n \to \infty} \sum_{i = 1}^{n}f(x^*_i)\Delta x$$ provided that this limit exists and gives the same value for all possible choices of sample points. If it does exist, we sat that $f$ is **integrable** on $[a, b]$

- $\int$: Integral sign
- $a$: Lower limit
- $b$: Upper limit
- $f(x)$: Integrand
- The procedure of calculating an integral is called **integration**


> [!NOTE] Theorem
> If $f$ is [[continuity|continuous]] on $[a, b]$, or if $f$ has only a finite number of jump discontinuities, then $f$ is integrable on $[a, b]$; that is, the definite integral $\int_{a}^{b}f(x)dx$ exists.

# Definite
1. $\int_{b}^{a} f(x) \, dx = -\int_{a}^{b} f(x) \, dx$

2. $\int_{a}^{a} f(x) \, dx = 0$

3. $\int_{a}^{b} c \, dx = c(b - a), \text{ where } c \text{ is any constan}$

4. $\int_{a}^{b} [f(x) + g(x)] \, dx = \int_{a}^{b} f(x) \, dx + \int_{a}^{b} g(x) \, dx$

5. $\int_{a}^{b} cf(x) \, dx = c \int_{a}^{b} f(x) \, dx, \text{ where } c \text{ is any constant}$

6. $\int_{a}^{b} [f(x) - g(x)] \, dx = \int_{a}^{b} f(x) \, dx - \int_{a}^{b} g(x) \, dx$

7. $\int_{a}^{c} f(x) \, dx + \int_{c}^{b} f(x) \, dx = \int_{a}^{b} f(x) \, dx$

**Comparison**

8. $\text{If } f(x) \geqslant 0 \text{ for } a \leqslant x \leqslant b, \text{ then } \int_{a}^{b} f(x) \, dx \geqslant 0$

9. $\text{If } f(x) \geqslant g(x) \text{ for } a \leqslant x \leqslant b, \text{ then } \int_{a}^{b} f(x) \, dx \geqslant \int_{a}^{b} g(x) \, dx$

10. $\text{If } m \leqslant f(x) \leqslant M \text{ for } a \leqslant x \leqslant b, \text{ then:}$
$$\\ m(b - a) \leqslant \int_{a}^{b} f(x) \, dx \leqslant M(b - a)$$

# Undefinite
$\int cf(x) \, dx = c \int f(x) \, dx$

$\int k \, dx = kx + C$

$\int \sin x \, dx = -\cos x + C$

$\int \sec^2 x \, dx = \tan x + C$

$\int \sec x \tan x \, dx = \sec x + C$

$\int [f(x) + g(x)] \, dx = \int f(x) \, dx + \int g(x) \, dx$

$\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$

$\int \cos x \, dx = \sin x + C$

$\int \csc^2 x \, dx = -\cot x + C$

$\int \csc x \cot x \, dx = -\csc x + C$