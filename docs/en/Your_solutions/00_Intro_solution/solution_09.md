To find the dimensions of the rectangle with the maximum area, we treat the upper-right corner of the rectangle as a point $(x, y)$ that lies on the curve $y = 3 - x^2$.

### 1. Define the Area Function
Since the rectangle is in the first quadrant and anchored to the axes (with one corner at the origin $(0,0)$ and the opposite corner at $(x, y)$):
* **Width:** $x$
* **Height:** $y = 3 - x^2$

The area $A$ is the product of the width and height:
$$A(x) = x \cdot (3 - x^2) = 3x - x^3$$

The domain for $x$ in the first quadrant is $[0, \sqrt{3}]$, as the curve intersects the x-axis at $x = \sqrt{3}$.



---

### 2. Find the Critical Points
To maximize the area, we take the derivative of $A(x)$ with respect to $x$ and set it to zero:
$$A'(x) = \frac{d}{dx}(3x - x^3) = 3 - 3x^2$$

Setting the derivative to zero:
$$3 - 3x^2 = 0 \implies 3x^2 = 3 \implies x^2 = 1$$

Since we are in the first quadrant ($x > 0$), we find:
$$x = 1$$

---

### 3. Determine the Dimensions and Maximum Area
Now, find the corresponding height $y$ and the maximum area $A$:
* **Width ($x$):** $1$
* **Height ($y$):** $3 - (1)^2 = 2$
* **Maximum Area:** $1 \times 2 = 2$

---

### 4. Verification
To ensure this is a maximum, we check the second derivative:
$$A''(x) = -6x$$
At $x=1$, $A''(1) = -6$. Since the second derivative is negative, the function is concave down, confirming that **$x=1$ is a local maximum**.

### Summary
The rectangle with the maximum area under the curve $y = 3 - x^2$ in the first quadrant has:
* **Width:** $1$ unit
* **Height:** $2$ units
* **Maximum Area:** $2$ square units