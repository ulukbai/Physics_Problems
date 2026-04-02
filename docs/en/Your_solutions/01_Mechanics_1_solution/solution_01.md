To analyze projectile motion, we decompose the initial velocity vector into its horizontal ($v_{0x}$) and vertical ($v_{0y}$) components. Using the approximation $\cos(37^\circ) \approx 0.8$ and $\sin(37^\circ) \approx 0.6$:

* $v_{0x} = 100 \cos(37^\circ) = 80 \text{ m/s}$
* $v_{0y} = 100 \sin(37^\circ) = 60 \text{ m/s}$

---

### 1. Differential Equations of Motion
Assuming the only force acting is gravity ($g \approx 9.81 \text{ m/s}^2$) acting in the negative $y$-direction:

**Horizontal Direction ($x$):**
There is no force, so acceleration is zero.
$$m\frac{d^2x}{dt^2} = 0 \implies \frac{dv_x}{dt} = 0$$

**Vertical Direction ($y$):**
Gravity acts downwards.
$$m\frac{d^2y}{dt^2} = -mg \implies \frac{dv_y}{dt} = -g$$



---

### 2. Time of Flight ($t_{total}$)
The projectile hits the ground when the vertical displacement $y(t) = 0$. 
Integrating the vertical acceleration twice gives:
$$y(t) = v_{0y}t - \frac{1}{2}gt^2$$

Setting $y(t) = 0$:
$$0 = t(v_{0y} - \frac{1}{2}gt) \implies t_{total} = \frac{2v_{0y}}{g}$$

$$t_{total} = \frac{2(60)}{9.81} \approx 12.23 \text{ s}$$

---

### 3. Maximum Height ($H$)
Maximum height occurs when the vertical velocity $v_y(t) = 0$. This happens at exactly half the time of flight ($t_{up} \approx 6.115 \text{ s}$).
Using the formula $H = \frac{v_{0y}^2}{2g}$:

$$H = \frac{60^2}{2(9.81)} = \frac{3600}{19.62} \approx 183.49 \text{ m}$$

---

### 4. Range ($R$)
The range is the horizontal distance traveled during the total time of flight. Since horizontal velocity is constant ($v_x = v_{0x}$):
$$R = v_{0x} \cdot t_{total}$$

$$R = 80 \cdot 12.23 \approx 978.4 \text{ m}$$

Alternatively, using the range formula $R = \frac{v_0^2 \sin(2\theta)}{g}$:
$$R = \frac{100^2 \sin(74^\circ)}{9.81} \approx \frac{10000 \cdot 0.961}{9.81} \approx 979.6 \text{ m}$$
*(Note: Small discrepancies are due to rounding the trigonometric values of $37^\circ$.)*