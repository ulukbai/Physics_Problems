To find the resulting standing wave, we use the **Superposition Principle**, which states that the resultant displacement is the sum of the individual displacements: $y(x, t) = y_1(x, t) + y_2(x, t)$.

### 1. Deriving the Standing Wave Equation
We use the trigonometric identity for the sum of two sines:
$$\sin(\alpha) + \sin(\beta) = 2 \sin\left(\frac{\alpha + \beta}{2}\right) \cos\left(\frac{\alpha - \beta}{2}\right)$$

In this case:
* $\alpha = kx - \omega t$
* $\beta = kx + \omega t$

Applying the identity:
$$y(x, t) = A \left[ \sin(kx - \omega t) + \sin(kx + \omega t) \right]$$
$$y(x, t) = 2A \sin\left(\frac{kx - \omega t + kx + \omega t}{2}\right) \cos\left(\frac{kx - \omega t - (kx + \omega t)}{2}\right)$$
$$y(x, t) = 2A \sin(kx) \cos(-\omega t)$$

Since cosine is an even function ($\cos(-\theta) = \cos(\theta)$), the resulting equation for the standing wave is:
$$y(x, t) = [2A \sin(kx)] \cos(\omega t)$$

---

### 2. Identifying the Nodes
**Nodes** are the points along the wave where the displacement is always zero ($y = 0$). This occurs when the spatial part of the equation, $\sin(kx)$, is equal to zero.



The sine function is zero when its argument is an integer multiple of $\pi$:
$$kx = n\pi \quad \text{where } n = 0, 1, 2, \dots$$

Since the wave number is defined as $k = \frac{2\pi}{\lambda}$, we can solve for $x$:
$$\left(\frac{2\pi}{\lambda}\right)x = n\pi$$
$$x = \frac{n\lambda}{2}$$

**Positions of the nodes:**
Nodes occur at intervals of half a wavelength:
* $x = 0$
* $x = \frac{\lambda}{2}$
* $x = \lambda$
* $x = \frac{3\lambda}{2}$
* ...and so on.

---

### Summary
* **Resulting Equation:** $y(x, t) = 2A \sin(kx) \cos(\omega t)$
* **Node Locations:** $x = \frac{n\lambda}{2}$ for $n = 0, 1, 2, \dots$