# Problem 2
# Escape Velocities and Cosmic Velocities

## 1. Definitions

**First Cosmic Velocity (Orbital Velocity):**

The minimum velocity needed for an object to stay in a stable circular orbit close to the surface of a celestial body without propulsion.

For Earth, this is approximately **7.9 km/s**.

**Second Cosmic Velocity (Escape Velocity):**

The minimum velocity needed to break free from the gravitational pull of a celestial body without further propulsion.

For Earth, this is approximately **11.2 km/s**.

**Third Cosmic Velocity (Heliocentric Escape Velocity):**

The minimum velocity needed to escape the gravitational influence of the Sun (or any star) from Earth orbit.

For Earth, this is about **16.7 km/s** relative to the Sun.

---

## 2. Mathematical Derivations

**First Cosmic Velocity (circular orbit velocity):**

\[
v_1 = \sqrt{\frac{GM}{r}}
\]

**Second Cosmic Velocity (escape velocity):**

\[
v_2 = \sqrt{2} \times v_1 = \sqrt{\frac{2GM}{r}}
\]

**Third Cosmic Velocity (leaving the solar system):**

To escape the Sun's gravity from a planet's orbit:

\[
v_3 = \sqrt{v_{\text{planet orbit}}^2 + v_{\text{escape from planet}}^2}
\]

where:

- $v_{\text{planet orbit}}$ is the orbital speed of the planet around the Sun.

**Parameters:**

- $G$ is the gravitational constant: $6.67430 \times 10^{-11} \, \text{m}^3\,\text{kg}^{-1}\,\text{s}^{-2}$
- $M$ is the mass of the celestial body
- $r$ is the radius (distance from the center of the body)

---

## 3. Python Code for Calculations and Visualization

```python
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

# Gravitational constant
G = 6.67430e-11  # m^3 kg^-1 s^-2

# Celestial body parameters: (mass in kg, radius in m)
bodies = {
    'Earth': (5.972e24, 6.371e6),
    'Mars': (6.39e23, 3.3895e6),
    'Jupiter': (1.898e27, 6.9911e7)
}

# Orbital speeds around the Sun (approximate) in m/s
orbital_speeds = {
    'Earth': 29.78e3,
    'Mars': 24.077e3,
    'Jupiter': 13.07e3
}

# Store results
results = {}

for body, (mass, radius) in bodies.items():
    v1 = np.sqrt(G * mass / radius)  # First cosmic velocity
    v2 = np.sqrt(2) * v1             # Second cosmic velocity
    v3 = np.sqrt(orbital_speeds[body]**2 + v2**2)  # Third cosmic velocity
    
    results[body] = {
        'First Cosmic Velocity (km/s)': v1 / 1000,
        'Second Cosmic Velocity (km/s)': v2 / 1000,
        'Third Cosmic Velocity (km/s)': v3 / 1000
    }

# Display results
df = pd.DataFrame(results).T
print(df)

# Plotting
df.plot(kind='bar', figsize=(10, 6))
plt.title('Cosmic Velocities for Different Celestial Bodies')
plt.ylabel('Velocity (km/s)')
plt.xticks(rotation=0)
plt.grid(True)
plt.tight_layout()
plt.show()
```
