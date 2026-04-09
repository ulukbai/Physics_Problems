```python?code_reference&code_event_index=2
f = 440
v_air = 343
v_water = 1482

lambda_air = v_air / f
lambda_water = v_water / f

print(f"{lambda_air=}")
print(f"{lambda_water=}")


```
```text?code_stdout&code_event_index=2
lambda_air=0.7795454545454545
lambda_water=3.368181818181818

```
To find the wavelength of the sound wave, we use the fundamental wave equation:

$$v = f \cdot \lambda$$

Where:
* $v$ is the speed of the wave (m/s)
* $f$ is the frequency (Hz)
* $\lambda$ (lambda) is the wavelength (m)

By rearranging the formula to solve for wavelength, we get:
$$\lambda = \frac{v}{f}$$



### 1. Wavelength in Air
Given:
* Frequency ($f$) = $440 \text{ Hz}$
* Speed in air ($v_{air}$) = $343 \text{ m/s}$

$$\lambda_{air} = \frac{343 \text{ m/s}}{440 \text{ Hz}} \approx 0.780 \text{ m}$$

### 2. Wavelength in Water
Given:
* Frequency ($f$) = $440 \text{ Hz}$ (Frequency remains constant when a wave moves from one medium to another)
* Speed in water ($v_{water}$) = $1482 \text{ m/s}$

$$\lambda_{water} = \frac{1482 \text{ m/s}}{440 \text{ Hz}} \approx 3.368 \text{ m}$$

[Image comparing sound wavelengths in air vs water]

### Summary
* The wavelength of the 440 Hz sound wave in **air** is approximately **$0.780 \text{ meters}$**.
* The wavelength of the same sound wave in **water** is approximately **$3.368 \text{ meters}$**.