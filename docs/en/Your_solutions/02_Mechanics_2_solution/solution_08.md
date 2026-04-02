To solve this, we look at the dynamics and energetics of a **Hooke's Law** force (like an ideal spring).

---

### 1. Equation of Motion and Solution
Using Newton's Second Law ($F = ma = m\frac{d^2x}{dt^2}$):
$$m\frac{d^2x}{dt^2} = -kx \implies \frac{d^2x}{dt^2} + \frac{k}{m}x = 0$$

This is a second-order linear differential equation. Let $\omega^2 = \frac{k}{m}$. The general solution is:
$$x(t) = A \cos(\omega t + \phi)$$
Where $A$ is the amplitude and $\phi$ is the phase constant.

---

### 2. Work Done from $0$ to $x_0$
Work ($W$) is the integral of force over displacement. Since the force varies with $x$, we calculate:
$$W = \int_{0}^{x_0} F(x) \, dx = \int_{0}^{x_0} (-kx) \, dx$$
$$W = -k \left[ \frac{1}{2}x^2 \right]_{0}^{x_0} = -\frac{1}{2}kx_0^2$$

---

### 3. Interpretation as Potential Energy
Potential energy ($U$) is defined as the negative of the work done by a conservative force ($U = -W$).
If we set the reference point $U(0) = 0$:
$$U(x) = \frac{1}{2}kx^2$$
This result shows that the energy stored in the system increases quadratically as the object is displaced from the equilibrium position ($x=0$).

---

### 4. Verify $F = -\frac{dU}{dx}$
To verify, we take the negative derivative of the potential energy function:
$$-\frac{d}{dx} \left( \frac{1}{2}kx^2 \right) = -\frac{1}{2}k (2x) = -kx$$
Since this matches our original force $F(x) = -kx$, the relationship is verified.

---

### 5. Graphs of $F(x)$ and $U(x)$



* **Force $F(x)$:** A straight line passing through the origin with a negative slope ($-k$). It is a **restoring force**, always pulling the object back toward $x=0$.
* **Potential Energy $U(x)$:** A **parabola** opening upward. It is always positive (or zero), indicating that work must be done to move the object away from equilibrium in either direction ($+x$ or $-x$).

---

**Pronunciation Guide for the formulas:**
* **$F = -kx$**: "Force equals negative kay ex."
* **$U = \frac{1}{2}kx^2$**: "Potential energy equals one-half kay ex squared."
* **$\frac{dU}{dx}$**: "The derivative of U with respect to x" or "dee-U dee-ex."