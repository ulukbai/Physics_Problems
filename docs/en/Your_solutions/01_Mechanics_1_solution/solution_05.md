To solve this, we must use vector addition. The boat's velocity relative to the ground ($\vec{v}_{bg}$) is the sum of its velocity relative to the water ($\vec{v}_{bw}$) and the water's velocity relative to the ground ($\vec{v}_{wg}$).

### 1. Determining the Heading Angle
To travel **directly north**, the boat’s horizontal (east-west) velocity component relative to the ground must be **zero**. This means the boat must aim slightly **upstream (west)** to cancel out the river's eastward flow.

Let $\theta$ be the angle measured from the North direction toward the West.
* **River velocity ($v_{wg}$):** $2 \text{ m/s}$ [East]
* **Boat speed in still water ($v_{bw}$):** $5 \text{ m/s}$

We set up a right triangle where the hypotenuse is the boat's speed ($5 \text{ m/s}$) and the opposite side is the river's speed ($2 \text{ m/s}$):
$$\sin(\theta) = \frac{v_{wg}}{v_{bw}} = \frac{2}{5} = 0.4$$
$$\theta = \arcsin(0.4) \approx 23.58^\circ$$

**Result:** The boat should head approximately **23.6° West of North**.



---

### 2. Crossing Time
First, we find the magnitude of the boat's velocity directed straight across the river (the northward component, $v_{bg,y}$). We can use the Pythagorean theorem:
$$v_{bw}^2 = v_{wg}^2 + v_{bg,y}^2$$
$$5^2 = 2^2 + v_{bg,y}^2$$
$$25 = 4 + v_{bg,y}^2 \implies v_{bg,y} = \sqrt{21} \approx 4.58 \text{ m/s}$$

Now, we calculate the time ($t$) to cross the 200-meter width:
$$t = \frac{\text{Width}}{v_{bg,y}} = \frac{200}{\sqrt{21}}$$
$$t \approx \frac{200}{4.58} \approx 43.64 \text{ s}$$

**Result:** It will take approximately **43.6 seconds** to cross the river.

---

### Summary

| Variable | Value |
| :--- | :--- |
| **Heading Angle** | $23.6^\circ$ West of North |
| **Resultant Velocity (North)** | $\approx 4.58 \text{ m/s}$ |
| **Time to Cross** | $\approx 43.6 \text{ s}$ |