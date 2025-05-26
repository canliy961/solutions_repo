# Problem 1
# Measuring Earth's Gravitational Acceleration Using a Pendulum

## Objective

To determine the acceleration due to gravity $g$ by measuring the oscillation period of a simple pendulum made from a phone charger cable, and analyzing the uncertainties in measurement. This experiment reinforces the relationship between pendulum length and period and emphasizes real-world experimental practice.

---

## Background Theory

The motion of a simple pendulum (for small angles $\theta < 15^\circ$) is described by the equation:

$$T = 2\pi \sqrt{\frac{L}{g}}$$

Where:  
- $T$ is the period of one oscillation (in seconds)  
- $L$ is the length of the pendulum (in meters)  
- $g$ is the acceleration due to gravity (in m/s²)  

Rearranged to solve for $g$:

$$g = \frac{4\pi^2 L}{T^2}$$

---

## Apparatus and Materials

- Phone charger cable (approx. 0.6 meters)  
- Small weight (e.g., USB adapter or key)  
- Tape measure with 1 mm resolution (3 m long)  
- Smartphone stopwatch  
- Wall-mounted nail to suspend the pendulum  

---

## Procedure

### 1. Setup

- Secure the weight to one end of the charger cable.  
- Hang the charger from a wall-mounted nail.  
- Measure the length $L$ from the suspension point to the center of the weight:  
  $$L = 60.0 \ \text{cm} = 0.600 \ \text{m}$$  
- Tape measure resolution = 1 mm = 0.001 m  
- Uncertainty in length:  
  $$\Delta L = \frac{0.001}{2} = 0.0005 \ \text{m}$$

### 2. Data Collection

- Displace the pendulum by less than $15^\circ$ and release gently.  
- Measure the time for 10 full oscillations ($T_{10}$), and repeat 10 times:

| Trial | $T_{10}$ (s) |
|-------|--------------|
| 1     | 15.59        |
| 2     | 15.53        |
| 3     | 15.60        |
| 4     | 15.69        |
| 5     | 15.52        |
| 6     | 15.52        |
| 7     | 15.70        |
| 8     | 15.62        |
| 9     | 15.49        |
| 10    | 15.59        |

---

## Calculations

### Mean time for 10 oscillations:

$$\overline{T_{10}} = 15.58 \ \text{s}$$

### Standard deviation:

$$\sigma_T = 0.07 \ \text{s}$$

### Uncertainty in $T_{10}$:

$$\Delta T_{10} = \frac{0.07}{\sqrt{10}} = 0.022 \ \text{s}$$

### Period of one oscillation:

$$T = \frac{\overline{T_{10}}}{10} = \frac{15.58}{10} = 1.558 \ \text{s}$$

### Uncertainty in period:

$$\Delta T = \frac{0.022}{10} = 0.0022 \ \text{s}$$

### Calculated gravitational acceleration:

$$g = \frac{4\pi^2 \cdot 0.6}{(1.558)^2} \approx 9.75 \ \text{m/s}^2$$

---

## Uncertainty in $g$

Relative uncertainty:

$$
\frac{\Delta g}{g} = \sqrt{\left( \frac{\Delta L}{L} \right)^2 + \left( 2 \cdot \frac{\Delta T}{T} \right)^2}
= \sqrt{ \left( \frac{0.0005}{0.6} \right)^2 + \left( 2 \cdot \frac{0.0022}{1.558} \right)^2 }
$$

$$
\approx \sqrt{6.94 \times 10^{-7} + 7.98 \times 10^{-5}} \approx 0.0031
$$

Absolute uncertainty:

$$
\Delta g = 0.0031 \cdot 9.75 \approx 0.03 \ \text{m/s}^2
$$

---

## Final Result

$$
g = 9.75 \pm 0.03 \ \text{m/s}^2
$$

---

## Discussion

- The measured value is within **0.6%** of the accepted standard $g = 9.81 \ \text{m/s}^2$.
- **Timing uncertainty** (reaction delay, stopwatch resolution) is the dominant source of error.
- Using a **shorter pendulum** (0.6 m) increases sensitivity to timing error compared to longer pendulums, affecting precision.

---

## Conclusion

This experiment demonstrates that a basic setup using household items can produce a fairly accurate value for $g$, emphasizing the importance of repeated measurements and error analysis.

## My Colab (Canliy961)

[Measurements](https://colab.research.google.com/drive/1tXh7-1Dlv1jVkg5xT4q6p5ik7yRYPwdB#scrollTo=PEimH_Hpqt-Z)
