#calculus #integral #maths #trigonometric 
**Strategy for Evaluating $\int \sin^m x \cos^n x \, dx$**

(a) If the power of cosine is odd ($n = 2k + 1$), save one cosine factor and use $\cos^2 x = 1 - \sin^2 x$ to express the remaining factors in terms of sine:

$$
\begin{aligned}
\int \sin^m x \cos^{2k+1} x \, dx &= \int \sin^m x (\cos^2 x)^k \cos x \, dx \\
&= \int \sin^m x (1 - \sin^2 x)^k \cos x \, dx
\end{aligned}
$$

Then substitute $u = \sin x$.

(b) If the power of sine is odd ($m = 2k + 1$), save one sine factor and use $\sin^2 x = 1 - \cos^2 x$ to express the remaining factors in terms of cosine:

$$
\begin{aligned}
\int \sin^{2k+1} x \cos^n x \, dx &= \int (\sin^2 x)^k \cos^n x \sin x \, dx \\
&= \int (1 - \cos^2 x)^k \cos^n x \sin x \, dx
\end{aligned}
$$

Then substitute $u = \cos x$. [Note that if the powers of both sine and cosine are odd, either (a) or (b) can be used.]

(c) If the powers of both sine and cosine are even, use the half-angle identities

$$\sin^2 x = \frac{1}{2}(1 - \cos 2x) \qquad \cos^2 x = \frac{1}{2}(1 + \cos 2x)$$

It is sometimes helpful to use the identity

$$\sin x \cos x = \frac{1}{2} \sin 2x$$

---

**Strategy for Evaluating $\int \tan^m x \sec^n x \, dx$**

(a) If the power of secant is even ($n = 2k, k \ge 2$), save a factor of $\sec^2 x$ and use $\sec^2 x = 1 + \tan^2 x$ to express the remaining factors in terms of $\tan x$:

$$
\begin{aligned}
\int \tan^m x \sec^{2k} x \, dx &= \int \tan^m x (\sec^2 x)^{k-1} \sec^2 x \, dx \\
&= \int \tan^m x (1 + \tan^2 x)^{k-1} \sec^2 x \, dx
\end{aligned}
$$

Then substitute $u = \tan x$.

(b) If the power of tangent is odd ($m = 2k + 1$), save a factor of $\sec x \tan x$ and use $\tan^2 x = \sec^2 x - 1$ to express the remaining factors in terms of $\sec x$:

$$
\begin{aligned}
\int \tan^{2k+1} x \sec^n x \, dx &= \int (\tan^2 x)^k \sec^{n-1} x \sec x \tan x \, dx \\
&= \int (\sec^2 x - 1)^k \sec^{n-1} x \sec x \tan x \, dx
\end{aligned}
$$

Then substitute $u = \sec x$.