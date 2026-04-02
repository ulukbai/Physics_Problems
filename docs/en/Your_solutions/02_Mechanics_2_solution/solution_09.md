To solve the motion of an object thrown vertically with linear air resistance, we treat this as a first-order linear differential equation. 

### 1. Analytical Solution

Starting with the equation of motion:
$$m \frac{dv}{dt} = -mg - kv$$

We can rewrite this to isolate the variables (separation of variables):
$$\frac{dv}{g + \frac{k}{m}v} = -dt$$

Integrating both sides from $t=0$ to $t$ and $v=v_0$ to $v(t)$:
$$\ln\left(g + \frac{k}{m}v\right) \bigg|_{v_0}^{v(t)} = -\frac{k}{m}t$$

Solving for $v(t)$, we get the **velocity function**:
$$v(t) = \left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t} - \frac{mg}{k}$$

To find the **position function** $x(t)$, we integrate $v(t)$ with respect to time, using the initial condition $x(0) = 10$:
$$x(t) = 10 + \int_{0}^{t} \left[\left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t'} - \frac{mg}{k}\right] dt'$$
$$x(t) = 10 + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right)(1 - e^{-\frac{k}{m}t}) - \frac{mg}{k}t$$

---

### 2. Maximum Height
The maximum height $H_{max}$ occurs when the velocity is zero ($v(t_{up}) = 0$). 

1. **Find time to peak ($t_{up}$):**
   $$0 = \left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t_{up}} - \frac{mg}{k} \implies t_{up} = \frac{m}{k} \ln\left(1 + \frac{kv_0}{mg}\right)$$

2. **Substitute $t_{up}$ into $x(t)$:**
   $$H_{max} = 10 + \frac{mv_0}{k} - \frac{m^2g}{k^2} \ln\left(1 + \frac{kv_0}{mg}\right)$$

---

### 3. Comparison with Vacuum (No Drag)
In a vacuum ($k=0$), the equations simplify via Taylor expansion or standard kinematics:

| Feature | With Drag ($k > 0$) | Without Drag ($k = 0$) |
| :--- | :--- | :--- |
| **Velocity** | Decays exponentially toward terminal velocity. | Decreases linearly ($v_0 - gt$). |
| **Max Height** | Lower (energy is lost to heat/friction). | Higher ($\frac{v_0^2}{2g}$). |
| **Symmetry** | Asymmetric; fall time > rise time. | Symmetric; fall time = rise time. |
| **Acceleration** | Decreases as velocity drops (during ascent). | Constant ($-g$). |



---

### 4. Numerical Simulation (Python)
This script uses `scipy` to solve the ODE and `matplotlib` to visualize the comparison.

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import odeint

# Constants
m = 1.0     # kg
g = 9.81    # m/s^2
k = 0.5     # drag coefficient
v0 = 20.0   # initial velocity m/s
x0 = 10.0   # initial height m
t = np.linspace(0, 4, 100)

# ODE with drag
def model_drag(y, t):
    v = y[1]
    dvdt = -g - (k/m)*v
    dxdt = v
    return [dxdt, dvdt]

# ODE without drag
def model_no_drag(y, t):
    return [y[1], -g]

# Solve
sol_drag = odeint(model_drag, [x0, v0], t)
sol_no_drag = odeint(model_no_drag, [x0, v0], t)

# Plotting
plt.figure(figsize=(10, 5))
plt.plot(t, sol_drag[:, 0], label=f'With Drag (k={k})', color='red')
plt.plot(t, sol_no_drag[:, 0], label='No Drag (Vacuum)', linestyle='--', color='blue')
plt.axhline(0, color='black', lw=1)
plt.title("Vertical Throw: Drag vs. Vacuum")
plt.xlabel("Time (s)")
plt.ylabel("Height (m)")
plt.ylim(0, max(sol_no_drag[:,0]) + 5)
plt.legend()
plt.grid(True)
plt.show()
```