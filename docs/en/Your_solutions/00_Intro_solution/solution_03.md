```python?code_reference&code_event_index=2
def calculate_gravity_factor(m1_factor, m2_factor, r_factor):
    # F = G * (m1 * m2) / r^2
    # New force F' = G * (m1*m1_factor * m2*m2_factor) / (r*r_factor)^2
    # F' / F = (m1_factor * m2_factor) / (r_factor^2)
    return (m1_factor * m2_factor) / (r_factor**2)

m1_f = 0.5
m2_f = 0.5
r_f = 2.0

factor = calculate_gravity_factor(m1_f, m2_f, r_f)
print(f"{factor=}")
print(f"Fraction: {factor.as_integer_ratio()}")


```
```text?code_stdout&code_event_index=2
factor=0.0625
Fraction: (1, 16)

```
To find the factor by which the gravitational force $F$ changes, we can examine the relationships in the formula for the **Universal Law of Gravitation**:

$$F = G \frac{m_1 m_2}{r^2}$$






### Step 1: Identify the changes
Let's denote the initial force as $F_1$ and the new force as $F_2$. The changes given are:
* The mass $m_1$ is halved: $m_1' = \frac{1}{2}m_1$
* The mass $m_2$ is halved: $m_2' = \frac{1}{2}m_2$
* The distance $r$ is doubled: $r' = 2r$

### Step 2: Set up the proportionality
The force $F$ is **directly proportional** to the product of the masses ($m_1 \cdot m_2$) and **inversely proportional** to the square of the distance ($r^2$).





Substitute the new values into the original formula to find $F_2$:

$$F_2 = G \frac{(\frac{1}{2}m_1) (\frac{1}{2}m_2)}{(2r)^2}$$

### Step 3: Simplify the expression
Multiply the factors in the numerator and calculate the square in the denominator:

$$F_2 = G \frac{\frac{1}{4} m_1 m_2}{4 r^2}$$

Now, separate the constants from the original variables:

$$F_2 = \left( \frac{\frac{1}{4}}{4} \right) \cdot G \frac{m_1 m_2}{r^2}$$
$$F_2 = \left( \frac{1}{4} \cdot \frac{1}{4} \right) \cdot F_1$$
$$F_2 = \frac{1}{16} F_1$$

### Conclusion
If the distance is doubled and both masses are halved, the gravitational force $F$ decreases by a **factor of $\frac{1}{16}$** (or $0.0625$ times its original value).