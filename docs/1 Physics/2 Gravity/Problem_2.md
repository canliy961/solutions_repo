# Problem 2
# Escape Velocities and Cosmic Velocities

## 1. Definitions

**First Cosmic Velocity (Orbital velocity):**  
The minimum velocity required for an object to achieve a stable circular orbit just above the surface of a celestial body.

$$
v_1 = \sqrt{\frac{GM}{R}}
$$

**Second Cosmic Velocity (Escape velocity):**  
The minimum velocity needed to completely escape the gravitational pull of a celestial body, without further propulsion.

$$
v_2 = \sqrt{2} \times v_1 = \sqrt{\frac{2GM}{R}}
$$

**Third Cosmic Velocity (Solar system escape velocity):**  
The velocity needed to escape not just the Earth but also the Sun's gravitational pull from Earth's orbit.

---

## 2. Mathematical Derivations

From Newtonian gravity:

$$
F = \frac{GMm}{r^2}
$$

Equating gravitational force to centripetal force for circular motion gives:

$$
\frac{mv^2}{r} = \frac{GMm}{r^2}
$$

Solving for $v$ gives the **first cosmic velocity**:

$$
v_1 = \sqrt{\frac{GM}{r}}
$$

For **escape velocity**, the kinetic energy must equal the gravitational potential energy:

$$
\frac{1}{2}mv^2 = \frac{GMm}{r}
$$

Solving for $v$ gives the **second cosmic velocity**:

$$
v_2 = \sqrt{\frac{2GM}{r}}
$$

The **third cosmic velocity** requires calculating the escape speed from the Sun, considering Earth's orbital velocity around the Sun (about 30 km/s).

---

## 3. Python Simulation and Visualization

```python
# cosmic_velocities.py

import numpy as np
import matplotlib.pyplot as plt

# Gravitational constant
G = 6.67430e-11  # m^3 kg^-1 s^-2

# Celestial bodies data: (Mass in kg, Radius in meters)
bodies = {
    "Earth": (5.972e24, 6.371e6),
    "Mars": (6.417e23, 3.3895e6),
    "Jupiter": (1.898e27, 6.9911e7)
}

def compute_velocities(M, R):
    v1 = np.sqrt(G * M / R)      # First cosmic velocity
    v2 = np.sqrt(2) * v1          # Second cosmic velocity
    return v1, v2

# Store results
results = {}

for body, (M, R) in bodies.items():
    v1, v2 = compute_velocities(M, R)
    results[body] = (v1, v2)

# Display results
for body, (v1, v2) in results.items():
    print(f"{body}:")
    print(f"  First Cosmic Velocity (orbital) = {v1/1000:.2f} km/s")
    print(f"  Second Cosmic Velocity (escape) = {v2/1000:.2f} km/s\n")

# Plotting
labels = list(results.keys())
v1_values = [results[body][0]/1000 for body in labels]  # in km/s
v2_values = [results[body][1]/1000 for body in labels]  # in km/s

x = np.arange(len(labels))
width = 0.35

fig, ax = plt.subplots()
rects1 = ax.bar(x - width/2, v1_values, width, label='First Cosmic Velocity')
rects2 = ax.bar(x + width/2, v2_values, width, label='Second Cosmic Velocity')

ax.set_ylabel('Velocity (km/s)')
ax.set_title('Cosmic Velocities by Celestial Body')
ax.set_xticks(x)
ax.set_xticklabels(labels)
ax.legend()

plt.grid(True, linestyle='--', alpha=0.7)
plt.show()
```
