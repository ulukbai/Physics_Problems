Young's double-slit experiment is a cornerstone of wave physics, demonstrating how light (or any wave) creates an interference pattern. The equation you provided is the mathematical basis for this, where $A/r$ represents the amplitude of a spherical wave in 3D (following the inverse-square law for intensity).

### Physics Principles
* **Path Difference:** The pattern is determined by the difference in distance from each slit to a point on the screen.
* **Constructive Interference:** Occurs when the path difference is an integer multiple of the wavelength ($n\lambda$), resulting in bright "fringes."
* **Destructive Interference:** Occurs when the path difference is a half-integer multiple of the wavelength ($(n + 0.5)\lambda$), resulting in dark "fringes."




---

### Interactive Young's Experiment Simulation

This simulation uses a high-performance rendering approach. You can adjust the slit separation ($d$) and the wavelength ($\lambda$) in real-time to see how the interference fringes shift.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Young's Double Slit Interference</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: #050505; color: white; margin: 0; display: flex; flex-direction: column; align-items: center; }
        .controls { background: #1a1a1a; padding: 20px; width: 100%; display: flex; justify-content: center; gap: 30px; border-bottom: 2px solid #333; z-index: 10; }
        .control-group { display: flex; flex-direction: column; width: 200px; }
        label { font-size: 14px; margin-bottom: 8px; color: #aaa; }
        canvas { cursor: crosshair; }
        .val-display { color: #00ffcc; font-weight: bold; margin-left: 5px; }
        .info { position: absolute; bottom: 20px; left: 20px; background: rgba(0,0,0,0.7); padding: 10px; border-radius: 5px; font-size: 12px; pointer-events: none; }
    </style>
</head>
<body>

<div class="controls">
    <div class="control-group">
        <label>Slit Separation (d): <span id="dVal" class="val-display">40</span></label>
        <input type="range" id="dSlider" min="5" max="150" step="1" value="40">
    </div>
    <div class="control-group">
        <label>Wavelength (λ): <span id="lambdaVal" class="val-display">30</span></label>
        <input type="range" id="lambdaSlider" min="10" max="80" step="1" value="30">
    </div>
    <div class="control-group">
        <label>Frequency (ω): <span id="omegaVal" class="val-display">0.10</span></label>
        <input type="range" id="omegaSlider" min="0.02" max="0.2" step="0.01" value="0.1">
    </div>
</div>

<canvas id="waveCanvas"></canvas>

<div class="info">
    • Red/Cyan: Peaks and Troughs<br>
    • Black lines: Nodes (Destructive Interference)
</div>

<script>
    const canvas = document.getElementById('waveCanvas');
    const ctx = canvas.getContext('2d');
    
    let d = 40;        // Distance between slits
    let lambda = 30;   // Wavelength
    let omega = 0.1;   // Angular frequency
    let t = 0;         // Time
    const A = 1200;    // Amplitude constant

    function resize() {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight - 100;
    }
    window.addEventListener('resize', resize);
    resize();

    // Event Listeners
    document.getElementById('dSlider').oninput = (e) => { d = parseInt(e.target.value); document.getElementById('dVal').innerText = d; };
    document.getElementById('lambdaSlider').oninput = (e) => { lambda = parseInt(e.target.value); document.getElementById('lambdaVal').innerText = lambda; };
    document.getElementById('omegaSlider').oninput = (e) => { omega = parseFloat(e.target.value); document.getElementById('omegaVal').innerText = omega.toFixed(2); };

    function draw() {
        t += omega;
        const k = (2 * Math.PI) / lambda;
        const w = canvas.width;
        const h = canvas.height;
        const res = 3; // Resolution (pixel size)

        const slit1 = { x: 50, y: h / 2 - d / 2 };
        const slit2 = { x: 50, y: h / 2 + d / 2 };

        for (let x = 0; x < w; x += res) {
            for (let y = 0; y < h; y += res) {
                // Distance to slit 1
                const r1 = Math.sqrt((x - slit1.x)**2 + (y - slit1.y)**2) + 0.1;
                // Distance to slit 2
                const r2 = Math.sqrt((x - slit2.x)**2 + (y - slit2.y)**2) + 0.1;

                // Superposition equation
                const u1 = (A / r1) * Math.sin(k * r1 - t);
                const u2 = (A / r2) * Math.sin(k * r2 - t);
                const totalU = u1 + u2;

                // Color mapping
                const intensity = Math.max(-255, Math.min(255, totalU * 15));
                if (intensity > 0) {
                    ctx.fillStyle = `rgb(${intensity}, ${intensity*0.2}, ${intensity*0.3})`;
                } else {
                    ctx.fillStyle = `rgb(0, ${-intensity*0.6}, ${-intensity})`;
                }
                ctx.fillRect(x, y, res, res);
            }
        }

        // Draw the Slits
        ctx.fillStyle = "white";
        ctx.beginPath();
        ctx.arc(slit1.x, slit1.y, 4, 0, Math.PI*2);
        ctx.arc(slit2.x, slit2.y, 4, 0, Math.PI*2);
        ctx.fill();

        requestAnimationFrame(draw);
    }

    draw();
</script>
</body>
</html>
```

### Observation Guide
1.  **Change $d$ (Slit Separation):** As you increase the distance between the slits, notice that the interference fringes become narrower and more numerous.
2.  **Change $\lambda$ (Wavelength):** Increasing the wavelength (making the wave "longer") causes the fringes to spread apart. This is why red light (longer wavelength) produces a wider pattern than blue light.
3.  **Center Line:** Notice the central axis between the slits always shows constructive interference (a bright fringe), because the path difference there is zero.