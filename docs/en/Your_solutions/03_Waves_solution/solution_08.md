To determine which function describes a traveling wave, we check if they satisfy the **linear wave equation**:

$$\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}$$

A more intuitive "shortcut" is that any function of the form $y(x,t) = f(x \pm vt)$ is a solution to the wave equation, provided the function is twice differentiable.

---

### a) $y(x,t) = A \cos(kx^2 - \omega t)$
Let's check the derivatives:
* **Space derivatives:** $\frac{\partial y}{\partial x} = -2kx A \sin(kx^2 - \omega t)$. The second derivative $\frac{\partial^2 y}{\partial x^2}$ will involve both $\sin$ and $\cos$ terms and depends on $x^2$.
* **Time derivatives:** $\frac{\partial^2 y}{\partial t^2} = -\omega^2 A \cos(kx^2 - \omega t)$.

Because the spatial part ($kx^2$) is non-linear, the $x$ and $t$ derivatives will not remain proportional by a constant $v^2$ across all points. 
**Result:** This does **not** describe a standard traveling wave.

---

### b) $y(x,t) = A(x-vt)^2$
This follows the form $f(u)$ where $u = (x-vt)$. Let's test it:
* **Left side ($\frac{\partial^2 y}{\partial x^2}$):**
    * $\frac{\partial y}{\partial x} = 2A(x-vt)$
    * $\frac{\partial^2 y}{\partial x^2} = 2A$
* **Right side ($\frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}$):**
    * $\frac{\partial y}{\partial t} = 2A(x-vt)(-v) = -2Av(x-vt)$
    * $\frac{\partial^2 y}{\partial t^2} = -2Av(-v) = 2Av^2$
    * $\frac{1}{v^2}(2Av^2) = 2A$

**Result:** Since $2A = 2A$, this **is** a valid solution. It represents a parabolic pulse traveling in the positive x-direction.

---

### c) $y(x,t) = A \log(x+vt)$
This also follows the form $f(u)$ where $u = (x+vt)$.
* **Left side:** $\frac{\partial^2 y}{\partial x^2} = -\frac{A}{(x+vt)^2}$
* **Right side:** $\frac{\partial^2 y}{\partial t^2} = -\frac{Av^2}{(x+vt)^2}$
    * $\frac{1}{v^2} \left(-\frac{Av^2}{(x+vt)^2}\right) = -\frac{A}{(x+vt)^2}$

**Result:** This **is** a valid solution. Mathematically, it satisfies the wave equation and represents a wave traveling in the negative x-direction (though physically, it would only be valid where $x+vt > 0$).

---

### Summary
Both **(b)** and **(c)** describe traveling waves because they are functions of the composite variable $(x \pm vt)$. Function **(a)** fails because the $x$ variable is squared inside the argument, which changes the shape of the wave as it moves (dispersion/distortion).