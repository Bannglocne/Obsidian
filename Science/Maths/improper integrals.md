#calculus #maths #integral 
# Type 1

**(a)** If $\int_a^t f(x)\, dx$ exists for every number $t \geq a$, then

$$\int_a^{\infty} f(x)\, dx = \lim_{t \to \infty} \int_a^t f(x)\, dx$$

provided this [[limit]] exists (as a finite number).

**(b)** If $\int_t^b f(x)\, dx$ exists for every number $t \leq b$, then

$$\int_{-\infty}^{b} f(x)\, dx = \lim_{t \to -\infty} \int_t^b f(x)\, dx$$

provided this [[limit]] exists (as a finite number).

The improper integrals $\int_a^{\infty} f(x)\, dx$ and $\int_{-\infty}^{b} f(x)\, dx$ are called **convergent** if the corresponding [[limit]] exists and **divergent** if the [[limit]] does not exist.

**(c)** If both $\int_a^{\infty} f(x)\, dx$ and $\int_{-\infty}^{a} f(x)\, dx$ are convergent, then we define

$$\int_{-\infty}^{\infty} f(x)\, dx = \int_{-\infty}^{a} f(x)\, dx + \int_a^{\infty} f(x)\, dx$$

In part (c) any real number $a$ can be used (see Exercise 74).

> [!NOTE]
> $$\int_1^{\infty} \frac{1}{x^p}\, dx \quad \text{is convergent if } p > 1 \text{ and divergent if } p \leq 1.$$

---

# Type 2

**(a)** If $f$ is continuous on $[a, b)$ and is discontinuous at $b$, then

$$\int_a^b f(x)\, dx = \lim_{t \to b^-} \int_a^t f(x)\, dx$$

if this [[limit]] exists (as a finite number).

**(b)** If $f$ is continuous on $(a, b]$ and is discontinuous at $a$, then

$$\int_a^b f(x)\, dx = \lim_{t \to a^+} \int_t^b f(x)\, dx$$

if this [[limit]] exists (as a finite number).

The improper integral $\int_a^b f(x)\, dx$ is called **convergent** if the corresponding [[limit]] exists and **divergent** if the [[limit]] does not exist.

**(c)** If $f$ has a discontinuity at $c$, where $a < c < b$, and both $\int_a^c f(x)\, dx$ and $\int_c^b f(x)\, dx$ are convergent, then we define

$$\int_a^b f(x)\, dx = \int_a^c f(x)\, dx + \int_c^b f(x)\, dx$$

---