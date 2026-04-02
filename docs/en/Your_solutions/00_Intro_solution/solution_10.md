To determine the final position of the ant, we need to separate its movement into horizontal ($x$) and vertical ($y$) components. The ant's steps follow the harmonic sequence $\frac{1}{n}$, but the direction rotates every 90 degrees.

### 1. Horizontal Component ($x$)
The ant moves East (positive $x$) on steps 1, 5, 9... and West (negative $x$) on steps 3, 7, 11...
The $x$-coordinate is the sum:
$$x = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots = \sum_{k=0}^{\infty} \frac{(-1)^k}{2k+1}$$

This is a famous infinite series known as the **Gregory-Leibniz series**. It converges to:
$$x = \frac{\pi}{4} \approx 0.785\text{ m}$$

---

### 2. Vertical Component ($y$)
The ant moves North (positive $y$) on steps 2, 6, 10... and South (negative $y$) on steps 4, 8, 12...
The $y$-coordinate is the sum:
$$y = \frac{1}{2} - \frac{1}{4} + \frac{1}{6} - \frac{1}{8} + \dots = \frac{1}{2} \left( 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \dots \right)$$

The term in the parentheses is the **alternating harmonic series**, which converges to $\ln(2)$. Therefore:
$$y = \frac{1}{2} \ln(2) = \ln(\sqrt{2}) \approx 0.347\text{ m}$$

---

### 3. Final Position
The ant eventually settles at a single point as the steps become infinitesimally small.



**Exact Coordinates:**
$$\left( \frac{\pi}{4}, \frac{\ln(2)}{2} \right)$$

**Numerical Approximation:**
The ant's final position is approximately **(0.785, 0.347)**. 

### Summary Table

| Direction | Series | Convergence Value |
| :--- | :--- | :--- |
| **East-West ($x$)** | $1 - 1/3 + 1/5 - \dots$ | $\pi/4$ |
| **North-South ($y$)** | $1/2 - 1/4 + 1/6 - \dots$ | $\ln(2)/2$ |

