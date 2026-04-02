To find the velocity and position, we will integrate the acceleration derived from Newton's Second Law, $\mathbf{F} = m\mathbf{a}$. Given $m = 3$ kg, the acceleration is:

$$\mathbf{a}(t) = \frac{\mathbf{F}(t)}{m} = \left( \frac{15t}{3}, \frac{3t-12}{3}, \frac{-6t^2}{3} \right) = (5t, t-4, -2t^2)$$

---

### 1. Particle's Velocity ($\mathbf{v}$)
We find the velocity by integrating the acceleration with respect to time:
$$\mathbf{v}(t) = \int \mathbf{a}(t) \, dt = \left( \int 5t \, dt, \int (t-4) \, dt, \int -2t^2 \, dt \right)$$

$$\mathbf{v}(t) = \left( \frac{5}{2}t^2 + C_1, \frac{1}{2}t^2 - 4t + C_2, -\frac{2}{3}t^3 + C_3 \right)$$

Using initial conditions $\mathbf{v}(0) = (2, 0, 1)$:
* $v_x(0) = 0 + C_1 = 2 \implies C_1 = 2$
* $v_y(0) = 0 - 0 + C_2 = 0 \implies C_2 = 0$
* $v_z(0) = 0 + C_3 = 1 \implies C_3 = 1$

**Velocity Dependence:**
$$\mathbf{v}(t) = \left( \frac{5}{2}t^2 + 2 \right)\mathbf{i} + \left( \frac{1}{2}t^2 - 4t \right)\mathbf{j} + \left( 1 - \frac{2}{3}t^3 \right)\mathbf{k}$$

---

### 2. Particle's Position ($\mathbf{r}$)
We find the position by integrating the velocity:
$$\mathbf{r}(t) = \int \mathbf{v}(t) \, dt = \left( \int (\frac{5}{2}t^2 + 2) \, dt, \int (\frac{1}{2}t^2 - 4t) \, dt, \int (1 - \frac{2}{3}t^3) \, dt \right)$$

$$\mathbf{r}(t) = \left( \frac{5}{6}t^3 + 2t + D_1, \frac{1}{6}t^3 - 2t^2 + D_2, t - \frac{2}{12}t^4 + D_3 \right)$$

Using initial conditions $\mathbf{r}(0) = (5, 2, -3)$:
* $x(0) = 0 + 0 + D_1 = 5 \implies D_1 = 5$
* $y(0) = 0 - 0 + D_2 = 2 \implies D_2 = 2$
* $z(0) = 0 - 0 + D_3 = -3 \implies D_3 = -3$

**Position Dependence:**
$$\mathbf{r}(t) = \left( \frac{5}{6}t^3 + 2t + 5 \right)\mathbf{i} + \left( \frac{1}{6}t^3 - 2t^2 + 2 \right)\mathbf{j} + \left( -\frac{1}{6}t^4 + t - 3 \right)\mathbf{k}$$

---

### Summary of Results

| Component | Velocity $v(t)$ | Position $r(t)$ |
| :--- | :--- | :--- |
| **x** | $\frac{5}{2}t^2 + 2$ | $\frac{5}{6}t^3 + 2t + 5$ |
| **y** | $\frac{1}{2}t^2 - 4t$ | $\frac{1}{6}t^3 - 2t^2 + 2$ |
| **z** | $1 - \frac{2}{3}t^3$ | $-\frac{1}{6}t^4 + t - 3$ |