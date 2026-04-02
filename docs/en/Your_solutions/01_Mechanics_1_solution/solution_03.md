To determine if Alice and Bob collide or how close they get, we must distinguish between their **paths** (the geometric tracks they leave) and their **actual positions** at a specific time $t$.

### 1. Do the Paths Intersect?
The paths intersect if there exist two times, $t_1$ and $t_2$, such that $A(t_1) = B(t_2)$.
Setting the coordinates equal:
1. $2 + t_1 = 2t_2 - 1 \implies t_1 = 2t_2 - 3$
2. $8 - 3t_1 = 2t_2 + 2$

Substitute (1) into (2):
$$8 - 3(2t_2 - 3) = 2t_2 + 2$$
$$8 - 6t_2 + 9 = 2t_2 + 2$$
$$17 - 6t_2 = 2t_2 + 2 \implies 15 = 8t_2 \implies t_2 = 1.875$$
$$t_1 = 2(1.875) - 3 = 0.75$$

The **paths intersect** at the point $B(1.875) = A(0.75) = (2.75, 5.75)$.

---

### 2. Do they Collide?
A collision only occurs if they are at the same point at the **same time** ($t_1 = t_2$).
As shown above, Alice reaches the intersection point at $t=0.75$, while Bob reaches it much later at $t=1.875$. 

**Conclusion:** They do **not** collide.

---

### 3. Minimum Distance and Timing
To find the minimum distance, we analyze the distance squared function $D^2(t)$ between $A(t)$ and $B(t)$:
$$\vec{d}(t) = A(t) - B(t) = (2+t - (2t-1), 8-3t - (2t+2))$$
$$\vec{d}(t) = (3 - t, 6 - 5t)$$

The square of the distance is:
$$f(t) = D^2 = (3-t)^2 + (6-5t)^2$$
$$f(t) = (9 - 6t + t^2) + (36 - 60t + 25t^2)$$
$$f(t) = 26t^2 - 66t + 45$$

To find the minimum, take the derivative and set it to zero:
$$f'(t) = 52t - 66 = 0$$
$$t = \frac{66}{52} \approx 1.269\ \text{s}$$



**Calculating the minimum distance:**
Substitute $t \approx 1.269$ back into $f(t)$:
$$D^2 = 26(1.269)^2 - 66(1.269) + 45 \approx 3.115$$
$$D_{min} = \sqrt{3.115} \approx 1.765\ \text{units}$$

---

### Summary Table

| Parameter | Result |
| :--- | :--- |
| **Path Intersection** | Yes, at $(2.75, 5.75)$ |
| **Collision** | No (they reach the point at different times) |
| **Time of Min. Distance** | $t \approx 1.27\ \text{s}$ |
| **Minimum Distance** | $\approx 1.77\ \text{units}$ |