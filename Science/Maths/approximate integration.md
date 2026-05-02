#calculus #maths #integral 
#  Midpoint Rule

$$\int_a^b f(x) \, dx \approx M_n = \Delta x [ f(\bar{x}_1) + f(\bar{x}_2) + \cdots + f(\bar{x}_n) ]$$

where $\qquad \Delta x = \frac{b - a}{n}$

and $\qquad \bar{x}_i = \frac{1}{2}(x_{i-1} + x_i) = \text{midpoint of } [x_{i-1}, x_i]$

---

# Trapezoidal Rule

$$\int_a^b f(x) \, dx \approx T_n = \frac{\Delta x}{2} [ f(x_0) + 2f(x_1) + 2f(x_2) + \cdots + 2f(x_{n-1}) + f(x_n) ]$$

where $\Delta x = (b - a)/n$ and $x_i = a + i\Delta x$.


**Error Bounds** Suppose $|f''(x)| \le K$ for $a \le x \le b$. If $E_T$ and $E_M$ are the errors in the Trapezoidal and Midpoint Rules, then

$$|E_T| \le \frac{K(b - a)^3}{12n^2} \quad \text{and} \quad |E_M| \le \frac{K(b - a)^3}{24n^2}$$

---

# Simpson's Rule

$$
\begin{aligned}
\int_a^b f(x) \, dx \approx S_n &= \frac{\Delta x}{3} [ f(x_0) + 4f(x_1) + 2f(x_2) + 4f(x_3) + \cdots \\
&\quad + 2f(x_{n-2}) + 4f(x_{n-1}) + f(x_n) ]
\end{aligned}
$$

where $n$ is even and $\Delta x = (b - a)/n$.


**Error Bound for Simpson's Rule** Suppose that $|f^{(4)}(x)| \le K$ for $a \le x \le b$. If $E_S$ is the error involved in using Simpson's Rule, then

$$|E_S| \le \frac{K(b - a)^5}{180n^4}$$