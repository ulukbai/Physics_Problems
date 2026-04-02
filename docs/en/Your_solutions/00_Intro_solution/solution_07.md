This is a classic "trap" problem that can be solved either through a complex infinite series or a very simple logical insight. While you *could* sum up every individual trip the fly makes, there is a much faster way.

### 1. The Logical Shortcut
The key is to focus on **time** rather than the individual distances of each back-and-forth flight. Since the fly stops moving exactly when the bicycle hits the wall, we only need to know how long the bicycle was moving.

* **Bicycle's Time ($t$):**
    The bicycle travels $10\text{ meters}$ at a speed of $1\text{ m/s}$.
    $$t = \frac{\text{Distance}}{\text{Speed}} = \frac{10\text{ m}}{1\text{ m/s}} = 10\text{ seconds}$$

* **Fly's Total Distance ($d$):**
    The fly is in the air for those same $10\text{ seconds}$, moving at a constant speed of $2\text{ m/s}$ (regardless of its direction).
    $$d = \text{Speed}_{\text{fly}} \times t = 2\text{ m/s} \times 10\text{ s} = 20\text{ meters}$$

**Result:** The fly travels a total of **20 meters**.

---

### 2. The Infinite Series Approach (The "Hard" Way)
If you prefer to see how the math balances out, you can calculate the distance of each segment. 

1.  **First leg (to the wall):** The fly (at $2\text{ m/s}$) and the wall (stationary) are $10\text{ m}$ apart. It takes $5\text{ s}$ to hit the wall. Distance = $10\text{ m}$.
2.  **Second leg (back to bike):** During those $5\text{ s}$, the bike moved $5\text{ m}$ closer. The fly and bike now head toward each other at a combined speed of $2 + 1 = 3\text{ m/s}$ over a remaining gap of $5\text{ m}$. Time = $5/3\text{ s}$. Distance = $10/3\text{ m}$.



This creates a geometric series where each round trip is a fraction of the previous one. Summing these segments $d_1 + d_2 + d_3 \dots$ will eventually converge to exactly **20 meters**.

---

### Fun Fact
Legend has it that this problem was once posed to the famous mathematician **John von Neumann**. He answered "20 meters" almost instantly. When asked if he knew the "time" trick, he replied, "Trick? I just summed the infinite series in my head."