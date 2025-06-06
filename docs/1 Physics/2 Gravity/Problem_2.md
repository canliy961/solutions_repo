# Problem 2
# Escape Velocities and Cosmic Velocities

# 1. Definitions

## Cosmic Velocities: Derivation, Earth Values and Comparison

## A. Derivation of the Three Cosmic Velocities

### A.1 First Cosmic Velocity (Orbital Velocity)

The first cosmic velocity is the minimum speed needed for an object to stay in a stable circular orbit just above the surface of a planet.

The gravitational force between the planet and the object provides the necessary centripetal force for the orbit:

Gravitational force:

$$
F_{\text{gravity}} = \frac{G M m}{r^2}
$$

Centripetal force:

$$
F_{\text{centripetal}} = \frac{m v^2}{r}
$$

Setting them equal:

$$
\frac{G M m}{r^2} = \frac{m v^2}{r}
$$

Cancel $m$ and rearrange:

$$
v^2 = \frac{G M}{r}
$$

Taking the square root:

$$
v = \sqrt{\frac{G M}{r}}
$$

Thus, the first cosmic velocity is:

$$
v_1 = \sqrt{\frac{G M}{r}}
$$

---

### A.2 Second Cosmic Velocity (Escape Velocity)

The second cosmic velocity is the minimum speed required to completely escape a planet’s gravitational pull.

Using energy conservation:

Kinetic energy:

$$
E_{\text{kinetic}} = \frac{1}{2} m v^2
$$

Gravitational potential energy:

$$
E_{\text{potential}} = -\frac{G M m}{r}
$$

At escape, total energy = 0:

$$
\frac{1}{2} m v^2 - \frac{G M m}{r} = 0
$$

Simplifying:

$$
\frac{1}{2} v^2 = \frac{G M}{r}
$$

Multiply by 2:

$$
v^2 = \frac{2 G M}{r}
$$

Taking the square root:

$$
v = \sqrt{\frac{2 G M}{r}}
$$

Thus, the second cosmic velocity is:

$$
v_2 = \sqrt{2} \times v_1
$$

---

### A.3 Third Cosmic Velocity (Solar System Escape Velocity)

The third cosmic velocity is the speed needed to escape not just the planet but also the gravitational pull of the Sun, starting from the Earth's orbit.

The escape velocity from the Sun at Earth’s orbit is:

$$
v_{\text{sun-escape}} = \sqrt{\frac{2 G M_{\text{sun}}}{r_{\text{orbit}}}}
$$

However, because the Earth itself is moving at about 30 km/s around the Sun, the spacecraft already has that speed.

Thus, the additional speed needed is calculated based on energy addition, and the final result for escape from Earth's surface is approximately:

$$
v_3 \approx 16.7 \, \text{km/s}
$$

---

## B. Values of Three Cosmic Velocities for Earth

Using Earth’s data:

- Gravitational constant: $G = 6.67430 \times 10^{-11} \, \text{m}^3 \, \text{kg}^{-1} \, \text{s}^{-2}$
- Earth mass: $M = 5.972 \times 10^{24} \, \text{kg}$
- Earth radius: $r = 6.371 \times 10^6 \, \text{m}$

### Calculations:

First Cosmic Velocity:

$$
v_1 = \sqrt{\frac{G M}{r}} \approx 7.91 \, \text{km/s}
$$

Second Cosmic Velocity:

$$
v_2 = \sqrt{2} \times v_1 \approx 11.18 \, \text{km/s}
$$

Third Cosmic Velocity:

$$
v_3 \approx 16.7 \, \text{km/s}
$$

---

## C. Comparison: Earth, Moon, Mars, and Jupiter

### C.1 Physical Data

| Celestial Body | Mass (kg)             | Radius (m)          |
|----------------|------------------------|---------------------|
| Earth          | $5.972 \times 10^{24}$  | $6.371 \times 10^6$  |
| Moon           | $7.347 \times 10^{22}$  | $1.737 \times 10^6$  |
| Mars           | $6.417 \times 10^{23}$  | $3.3895 \times 10^6$ |
| Jupiter        | $1.898 \times 10^{27}$  | $6.9911 \times 10^7$ |

---

### C.2 Calculated Velocities

| Celestial Body | First Cosmic Velocity (km/s) | Second Cosmic Velocity (km/s) |
|----------------|------------------------------|-------------------------------|
| Earth          | 7.91                         | 11.18                         |
| Moon           | 1.68                         | 2.38                          |
| Mars           | 3.55                         | 5.02                          |
| Jupiter        | 42.08                        | 59.49                         |

---

![alt text](image-5.png)

# 2. Mathematical Derivations

## 2.1 Derivation of the First Cosmic Velocity (Orbital Velocity)

The first cosmic velocity is the minimum speed required for an object to maintain a stable circular orbit around a planet without falling back.

To find it, we equate:

- The gravitational force pulling the object toward the planet
- The centripetal force needed to keep the object moving in a circle.

Gravitational force:

$$
F_{\text{gravity}} = \frac{G M m}{r^2}
$$

Centripetal force:

$$
F_{\text{centripetal}} = \frac{m v_1^2}{r}
$$

Setting them equal:

$$
\frac{G M m}{r^2} = \frac{m v_1^2}{r}
$$

We can cancel $m$ from both sides:

$$
\frac{G M}{r^2} = \frac{v_1^2}{r}
$$

Multiplying both sides by $r$:

$$
\frac{G M}{r} = v_1^2
$$

Taking the square root:

$$
v_1 = \sqrt{\frac{G M}{r}}
$$

Thus, the first cosmic velocity formula is:

$$
v_1 = \sqrt{\frac{G M}{r}}
$$

---

## 2.2 Derivation of the Second Cosmic Velocity (Escape Velocity)

The second cosmic velocity is the minimum speed needed to completely escape the gravitational field of a planet without further propulsion.

To derive it, we use energy conservation:

- The object's initial kinetic energy must be enough to counterbalance the gravitational potential energy.

Initial kinetic energy:

$$
E_{\text{kinetic}} = \frac{1}{2} m v_2^2
$$

Gravitational potential energy:

$$
E_{\text{potential}} = -\frac{G M m}{r}
$$

At the point of escape, total energy = 0:

$$
E_{\text{kinetic}} + E_{\text{potential}} = 0
$$

Substituting:

$$
\frac{1}{2} m v_2^2 - \frac{G M m}{r} = 0
$$

Rearranging:

$$
\frac{1}{2} m v_2^2 = \frac{G M m}{r}
$$

Cancel $m$ from both sides:

$$
\frac{1}{2} v_2^2 = \frac{G M}{r}
$$

Multiplying both sides by 2:

$$
v_2^2 = \frac{2 G M}{r}
$$

Taking the square root:

$$
v_2 = \sqrt{\frac{2 G M}{r}}
$$

Thus, the second cosmic velocity is:

$$
v_2 = \sqrt{2} \times v_1
$$

---

## 2.3 Derivation of the Third Cosmic Velocity (Solar System Escape Velocity)

The third cosmic velocity is the minimum speed needed for an object to escape not only Earth's gravity, but also the Sun's gravitational pull, starting from Earth's orbit.

First, the escape velocity from the Sun at Earth's distance is:

$$
v_{\text{sun-escape}} = \sqrt{\frac{2 G M_{\text{sun}}}{r_{\text{orbit}}}}
$$

Where:

- $M_{\text{sun}}$ is the Sun's mass,
- $r_{\text{orbit}}$ is Earth's distance from the Sun (about $1.496 \times 10^{11} \, \text{m}$).

However, because the Earth is already moving around the Sun with an orbital speed of about 30 km/s, a spacecraft launched from Earth already has this speed.

Thus, the spacecraft needs enough additional velocity to make the total energy zero relative to the Sun.

The final approximate third cosmic velocity from Earth's surface, considering Earth's gravity and solar effects, is about:

$$
v_3 \approx 16.7 \, \text{km/s}
$$

---

## Quick Summary

| Velocity Type         | Derived Formula                        | Meaning                               |
|------------------------|----------------------------------------|---------------------------------------|
| First Cosmic Velocity  | $v_1 = \sqrt{\frac{G M}{r}}$            | Stay in circular orbit                |
| Second Cosmic Velocity | $v_2 = \sqrt{\frac{2 G M}{r}}$ or $v_2 = \sqrt{2} \times v_1$ | Escape planet's gravity              |
| Third Cosmic Velocity  | $v_3 \approx 16.7 \, \text{km/s}$       | Escape Sun's gravity from Earth's orbit |

---

# 3. Python Simulation and Visualization

```python
# cosmic_velocities.py

import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11  # gravitational constant, m^3 kg^-1 s^-2
M_earth = 5.972e24  # mass of Earth, kg
R_earth = 6.371e6  # radius of Earth, m

# Functions for velocities
def v1(M, r):
    return np.sqrt(G * M / r) / 1000  # in km/s

def v2(M, r):
    return np.sqrt(2 * G * M / r) / 1000  # in km/s

# Third cosmic velocity approximation (given)
v3_earth = 16.7  # km/s

# Generate data
radii = np.linspace(R_earth, 10 * R_earth, 500)  # From Earth's radius up to 10 times
v1_values = v1(M_earth, radii)
v2_values = v2(M_earth, radii)

# Plotting
plt.figure(figsize=(10, 6))
plt.plot(radii / 1e6, v1_values, label='First Cosmic Velocity (Orbital)', linestyle='-')
plt.plot(radii / 1e6, v2_values, label='Second Cosmic Velocity (Escape)', linestyle='--')
plt.axhline(y=v3_earth, color='r', linestyle=':', label='Third Cosmic Velocity (Solar Escape)')

plt.xlabel('Distance from Center of Earth (Million meters)')
plt.ylabel('Velocity (km/s)')
plt.title('Cosmic Velocities as a Function of Distance')
plt.legend()
plt.grid(True)
plt.show()
```

![alt text](image-6.png)

![alt text](image-7.png)

## My Colab (Canliy961)

[Cosmic Velocities](https://colab.research.google.com/drive/1V_AZtrpk5ewRWB0B5KvcSwBR-c_ZzB4-#scrollTo=ZljDH-xTKP9c)
