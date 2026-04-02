To show that the maximum range is achieved at $45^\circ$, we treat the range $R$ as a function of the launch angle $\theta$ and find its critical points using calculus.

### 1. The Range Equation
The analytical expression for the range $R$ of a projectile launched from the ground is:
$$R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$$

Here, $v_0$ (initial velocity) and $g$ (acceleration due to gravity) are constants. Therefore, the range depends entirely on the term $\sin(2\theta)$.

---

### 2. Analytical Derivation (Calculus Method)
To find the angle that maximizes $R(\theta)$, we take the first derivative with respect to $\theta$ and set it to zero:

$$\frac{dR}{d\theta} = \frac{v_0^2}{g} \cdot \frac{d}{d\theta}(\sin(2\theta))$$

Using the chain rule, $\frac{d}{d\theta}(\sin(2\theta)) = 2\cos(2\theta)$:
$$\frac{dR}{d\theta} = \frac{2v_0^2 \cos(2\theta)}{g}$$

**Set the derivative to zero to find the extremum:**
$$0 = \frac{2v_0^2 \cos(2\theta)}{g}$$

Since $v_0$ and $g$ are non-zero, we must have:
$$\cos(2\theta) = 0$$

The values for which the cosine function is zero are $90^\circ, 270^\circ, \dots$. For a physical launch angle:
$$2\theta = 90^\circ$$
$$\theta = 45^\circ$$

---

### 3. Verification (Second Derivative Test)
To ensure this is a maximum, we check the second derivative:
$$\frac{d^2R}{d\theta^2} = -\frac{4v_0^2 \sin(2\theta)}{g}$$

At $\theta = 45^\circ$:
$$\frac{d^2R}{d\theta^2} = -\frac{4v_0^2 \sin(90^\circ)}{g} = -\frac{4v_0^2}{g}$$

Since the second derivative is **negative**, the function has a local maximum at $\theta = 45^\circ$.



---

### 4. Intuitive Observation
Mathematically, the sine function reaches its maximum value of $1$ when its argument is $90^\circ$. 
$$\sin(X) = 1 \implies X = 90^\circ$$
In our range formula, the argument is $2\theta$. Therefore:
$$2\theta = 90^\circ \implies \theta = 45^\circ$$

At this angle, the projectile perfectly balances its "time in the air" (dictated by the vertical component) with its "horizontal speed," resulting in the furthest distance traveled.