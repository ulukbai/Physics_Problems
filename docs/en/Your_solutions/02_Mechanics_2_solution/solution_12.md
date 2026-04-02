Since the force and mass are constant, this is a classic case of uniformly accelerated motion in two dimensions.

### 1. Acceleration $\vec a(t)$
Using Newton's Second Law ($\vec F = m\vec a$):
$$\vec a = \frac{\vec F}{m} = \frac{[6, 2]}{2}$$

**Result:** $\vec a(t) = [3, 1]\ \text{m/s}^2$

---

### 2. Velocity $\vec v(t)$
We integrate the acceleration and apply the initial condition $\vec v(0) = (1, -1)$:
$$\vec v(t) = \int \vec a \, dt = [3t + C_1, t + C_2]$$
Substituting $t=0$: $[0+C_1, 0+C_2] = [1, -1] \implies C_1=1, C_2=-1$.

**Result:** $\vec v(t) = [3t + 1, t - 1]\ \text{m/s}$

---

### 3. Position $\vec r(t)$
We integrate the velocity and apply the initial condition $\vec r(0) = (0, 0)$:
$$\vec r(t) = \int \vec v(t) \, dt = \left[ \frac{3}{2}t^2 + t + D_1, \frac{1}{2}t^2 - t + D_2 \right]$$
Since $\vec r(0) = [0, 0]$, both constants $D_1$ and $D_2$ are $0$.

**Result:** $\vec r(t) = \left[ 1.5t^2 + t, 0.5t^2 - t \right]\ \text{m}$

---

### 4. Trajectory of the Motion
The trajectory is a **parabola**. To see this, you can solve for $t$ in one component and substitute it into the other, though in vector form, it is simply the path traced by $\vec r(t)$. Initially, the body moves slightly "down and right" before the constant force pulls it strongly into the first quadrant.



---

### 5. Work Done at $t = 3\ \text{s}$
Work for a constant force is $W = \vec F \cdot \Delta \vec r$.
First, find the position at $t = 3$:
* $x(3) = 1.5(3)^2 + 3 = 13.5 + 3 = 16.5\ \text{m}$
* $y(3) = 0.5(3)^2 - 3 = 4.5 - 3 = 1.5\ \text{m}$
So, $\Delta \vec r = [16.5, 1.5]$.

$$W = \vec F \cdot \Delta \vec r = (6 \times 16.5) + (2 \times 1.5)$$
$$W = 99 + 3 = 102\ \text{J}$$

---

### 6. Work-Energy Theorem Consistency
The theorem states $W = \Delta K = K_f - K_i$.

**Initial Kinetic Energy ($t=0$):**
$v(0)^2 = 1^2 + (-1)^2 = 2$
$$K_i = \frac{1}{2}mv(0)^2 = \frac{1}{2}(2)(2) = 2\ \text{J}$$

**Final Kinetic Energy ($t=3$):**
First, find $\vec v(3)$:
* $v_x(3) = 3(3) + 1 = 10$
* $v_y(3) = 3 - 1 = 2$
$v(3)^2 = 10^2 + 2^2 = 104$
$$K_f = \frac{1}{2}mv(3)^2 = \frac{1}{2}(2)(104) = 104\ \text{J}$$

**Change in Kinetic Energy:**
$$\Delta K = 104 - 2 = 102\ \text{J}$$

**Conclusion:** Since $W = 102\ \text{J}$ and $\Delta K = 102\ \text{J}$, the results are perfectly consistent.