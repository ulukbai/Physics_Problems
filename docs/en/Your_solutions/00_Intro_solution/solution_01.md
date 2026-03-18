```python?code_reference&code_event_index=2
import numpy as np

# 1. Vector Algebra
a = np.array([2, 1, -3])
b = np.array([4, -2, 1])

# a) Magnitudes
mag_a = np.linalg.norm(a)
mag_b = np.linalg.norm(b)

# b) Dot product
dot_prod = np.dot(a, b)

# c) Cross product
cross_prod = np.cross(a, b)

# d) Angle
cos_theta = dot_prod / (mag_a * mag_b)
angle_rad = np.arccos(cos_theta)
angle_deg = np.degrees(angle_rad)

# 2. Systems of Equations
# 2x + 3y = 12
# x - y = 1 -> x = y + 1
# 2(y + 1) + 3y = 12 -> 2y + 2 + 3y = 12 -> 5y = 10 -> y = 2
# x = 2 + 1 = 3

A = np.array([[2, 3], [1, -1]])
B = np.array([12, 1])
solution = np.linalg.solve(A, B)

print(f"{mag_a=}")
print(f"{mag_b=}")
print(f"{dot_prod=}")
print(f"{cross_prod=}")
print(f"{angle_deg=}")
print(f"{solution=}")


```
```text?code_stdout&code_event_index=2
mag_a=3.7416573867739413
mag_b=4.58257569495584
dot_prod=3
cross_prod=array([ -5, -14,  -8])
angle_deg=79.92346287144585
solution=array([3., 2.])

```
## 1. Vector Algebra

Given the vectors:
$\vec{a} = [2, 1, -3]$
$\vec{b} = [4, -2, 1]$

### a) Magnitude of each vector
The magnitude (or length) of a vector $[x, y, z]$ is calculated as $\sqrt{x^2 + y^2 + z^2}$.

* **Magnitude of $\vec{a}$:**
    $$|\vec{a}| = \sqrt{2^2 + 1^2 + (-3)^2} = \sqrt{4 + 1 + 9} = \sqrt{14} \approx 3.742$$

* **Magnitude of $\vec{b}$:**
    $$|\vec{b}| = \sqrt{4^2 + (-2)^2 + 1^2} = \sqrt{16 + 4 + 1} = \sqrt{21} \approx 4.583$$

### b) Dot product $\vec{a} \cdot \vec{b}$
The dot product is the sum of the products of the corresponding components:
$$\vec{a} \cdot \vec{b} = (2 \cdot 4) + (1 \cdot -2) + (-3 \cdot 1)$$
$$\vec{a} \cdot \vec{b} = 8 - 2 - 3 = 3$$



### c) Cross product $\vec{a} \times \vec{b}$
The cross product is found using the determinant of a $3 \times 3$ matrix:
$$\vec{a} \times \vec{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & -3 \\ 4 & -2 & 1 \end{vmatrix}$$

$$\vec{a} \times \vec{b} = \mathbf{i}(1 \cdot 1 - (-3)(-2)) - \mathbf{j}(2 \cdot 1 - (-3)(4)) + \mathbf{k}(2 \cdot -2 - 1 \cdot 4)$$
$$\vec{a} \times \vec{b} = \mathbf{i}(1 - 6) - \mathbf{j}(2 + 12) + \mathbf{k}(-4 - 4)$$
$$\vec{a} \times \vec{b} = [-5, -14, -8]$$



[Image of cross product of two vectors]


### d) Angle between vectors $\vec{a}$ and $\vec{b}$
The angle $\theta$ can be found using the formula $\vec{a} \cdot \vec{b} = |\vec{a}| |\vec{b}| \cos(\theta)$:
$$\cos(\theta) = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}| |\vec{b}|} = \frac{3}{\sqrt{14} \cdot \sqrt{21}} = \frac{3}{\sqrt{294}}$$
$$\theta = \arccos\left(\frac{3}{\sqrt{294}}\right) \approx 79.92^\circ$$

---

