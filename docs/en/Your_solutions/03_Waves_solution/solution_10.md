This is a fascinating visualization of **Huygens' Principle** and wave interference. The equation you provided represents a spherical (or cylindrical) wave originating from a point source, where $\alpha$ controls the intensity decay (geometric spreading). 

In physical terms:
* $\alpha = 0$: No decay (plane-wave-like behavior in 1D).
* $\alpha = 0.5$: Typical for cylindrical waves (2D).
* $\alpha = 1.0$: Typical for spherical waves (3D intensity follows inverse square, but amplitude follows $1/r$).

### Interactive Wave Interference Lab

This implementation uses a HTML5 Canvas. **Click anywhere on the black canvas to place a wave source.**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Wave Source Superposition</title>
    <style>
        body { font-family: sans-serif; background: #1a1a1a; color: white; display: flex; flex-direction: column; align-items: center; margin: 0; overflow: hidden; }
        canvas { background: #000; cursor: crosshair; box-shadow: 0 0 20px rgba(0,0,0,0.5); }
        .controls { background: rgba(255, 255, 255, 0.1); padding: 15px; width: 100%; display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; border-bottom: 1px solid #444; }
        .control-group { display: flex; flex-direction: column; align-items: center; }
        label { font-size: 12px; margin-bottom: 5px; color: #ccc; }
        span { font-family: monospace; color: #0af; }
    </style>
</head>
<body>

<div class="controls">
    <div class="control-group">
        <label>Decay (α): <span id="alphaVal">0.5</span></label>
        <input type="range" id="alpha" min="0" max="2" step="0.1" value="0.5">
    </div>
    <div class="control-group">
        <label>Wavenumber (k): <span id="kVal">0.2</span></label>
        <input type="range" id="k" min="0.05" max="0.5" step="0.01" value="0.2">
    </div>
    <div class="control-group">
        <label>Frequency (ω): <span id="omegaVal">5.0</span></label>
        <input type="range" id="omega" min="1" max="15" step="0.5" value="5">
    </div>
    <button onclick="sources = []">Clear Sources</button>
    <div style="margin-left: 20px; align-self: center;">Click canvas to add dots!</div>
</div>

<canvas id="waveCanvas"></canvas>

<script>
    const canvas = document.getElementById('waveCanvas');
    const ctx = canvas.getContext('2d');
    
    // Parameters
    let alpha = 0.5;
    let k = 0.2;
    let omega = 5.0;
    let t = 0;
    let sources = [];
    const A = 40; // Amplitude scaling

    // Resize canvas
    function resize() {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight - 80;
    }
    window.addEventListener('resize', resize);
    resize();

    // Input handling
    document.getElementById('alpha').addEventListener('input', e => { alpha = parseFloat(e.target.value); document.getElementById('alphaVal').innerText = alpha; });
    document.getElementById('k').addEventListener('input', e => { k = parseFloat(e.target.value); document.getElementById('kVal').innerText = k; });
    document.getElementById('omega').addEventListener('input', e => { omega = parseFloat(e.target.value); document.getElementById('omegaVal').innerText = omega; });

    canvas.addEventListener('mousedown', e => {
        sources.push({ x: e.clientX, y: e.clientY - 80 });
    });

    function animate() {
        t += 0.05;
        const w = canvas.width;
        const h = canvas.height;
        
        // We use a lower resolution grid for performance, then scale up
        const res = 4; 
        ctx.clearRect(0, 0, w, h);
        
        for (let x = 0; x < w; x += res) {
            for (let y = 0; y < h; y += res) {
                let u = 0;
                
                for (let s of sources) {
                    const dx = x - s.x;
                    const dy = y - s.y;
                    const r = Math.sqrt(dx*dx + dy*dy) + 0.1; // Avoid division by zero
                    
                    // Wave equation: u = (A / r^alpha) * sin(k*r - omega*t)
                    u += (A / Math.pow(r, alpha)) * Math.sin(k * r - omega * t);
                }

                if (sources.length > 0) {
                    // Map wave amplitude to color (Blue for negative, Red for positive)
                    const val = Math.max(-255, Math.min(255, u * 10));
                    const rCol = val > 0 ? val : 0;
                    const bCol = val < 0 ? -val : 0;
                    const gCol = Math.abs(val) * 0.2;
                    
                    ctx.fillStyle = `rgb(${rCol}, ${gCol}, ${bCol})`;
                    ctx.fillRect(x, y, res, res);
                }
            }
        }

        // Draw sources as small dots
        ctx.fillStyle = "white";
        for (let s of sources) {
            ctx.beginPath();
            ctx.arc(s.x, s.y, 3, 0, Math.PI * 2);
            ctx.fill();
        }

        requestAnimationFrame(animate);
    }

    animate();
</script>
</body>
</html>
```

### Key Observations for your investigation:
1.  **Constructive/Destructive Interference:** Place two dots close to each other. You will see "lanes" of high intensity and nodes where the waves cancel out.
2.  **Effect of $\alpha$:** * Set $\alpha = 0$: Notice how the waves maintain their full intensity even at the edges of the screen.
    * Set $\alpha = 2$: The waves will appear very "localized" around the dots, decaying almost instantly as they move away.
3.  **Huygens-Fresnel Principle:** Try placing a long line of dots. You will see them eventually form a single **plane wave** front, demonstrating how complex wave shapes are just the sum of point sources.