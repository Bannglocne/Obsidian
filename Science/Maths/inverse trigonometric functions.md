#calculus #maths #trigonometric
**sin**
$$
\sin^{-1} x = y \iff \sin y = x \quad \text{and} \quad -\frac{\pi}{2} \le y \le \frac{\pi}{2}
$$ 
$$
\sin^{-1}(\sin x) = x \quad \text{for } -\frac{\pi}{2} \le x \le \frac{\pi}{2}
$$
$$\sin(\sin^{-1} x) = x \quad \text{for } -1 \le x \le 1
$$ 
$$
\frac{d}{dx} (\sin^{-1} x) = \frac{1}{\sqrt{1 - x^2}} \quad -1 < x < 1
$$

**cos**
$$
\cos^{-1} x = y \iff \cos y = x \quad \text{and} \quad 0 \le y \le \pi
$$ 
$$
\cos^{-1}(\cos x) = x \quad \text{for } 0 \le x \le \pi
$$ 
$$
\cos(\cos^{-1} x) = x \quad \text{for } -1 \le x \le 1
$$ 
$$
\frac{d}{dx} (\cos^{-1} x) = -\frac{1}{\sqrt{1 - x^2}} \quad -1 < x < 1
$$

**tan**
$$
\tan^{-1} x = y \iff \tan y = x \quad \text{and} \quad -\frac{\pi}{2} < y < \frac{\pi}{2}
$$
$$
\lim_{x \to \infty} \tan^{-1} x = \frac{\pi}{2} \quad \quad \lim_{x \to -\infty} \tan^{-1} x = -\frac{\pi}{2}
$$
$$
\frac{d}{dx} (\tan^{-1} x) = \frac{1}{1 + x^2}
$$

**remaining**
$$
y = \csc^{-1} x \ (|x| \ge 1) \iff \csc y = x \quad \text{and} \quad y \in (0, \pi/2] \cup (\pi, 3\pi/2]
$$
$$
y = \sec^{-1} x \ (|x| \ge 1) \iff \sec y = x \quad \text{and} \quad y \in [0, \pi/2) \cup [\pi, 3\pi/2)
$$
$$
y = \cot^{-1} x \ (x \in \mathbb{R}) \iff \cot y = x \quad \text{and} \quad y \in (0, \pi)
$$
---
**[[derivatives]]**
$$
\frac{d}{dx} (\sin^{-1} x) = \frac{1}{\sqrt{1 - x^2}} \qquad \frac{d}{dx} (\csc^{-1} x) = -\frac{1}{x\sqrt{x^2 - 1}}
$$
$$
\frac{d}{dx} (\cos^{-1} x) = -\frac{1}{\sqrt{1 - x^2}} \qquad \frac{d}{dx} (\sec^{-1} x) = \frac{1}{x\sqrt{x^2 - 1}}
$$
$$
\frac{d}{dx} (\tan^{-1} x) = \frac{1}{1 + x^2} \qquad \frac{d}{dx} (\cot^{-1} x) = -\frac{1}{1 + x^2}
$$

**[[integral]]**
$$
\int \frac{1}{\sqrt{1 - x^2}} \, dx = \sin^{-1} x + C
$$
$$
\int \frac{1}{x^2 + 1} \, dx = \tan^{-1} x + C
$$

$$
\int \frac{1}{x^2 + a^2} \, dx = \frac{1}{a} \tan^{-1} \left( \frac{x}{a} \right) + C
$$