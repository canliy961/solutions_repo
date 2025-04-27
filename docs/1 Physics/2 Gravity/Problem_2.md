# Problem 2
# Escape Velocities and Cosmic Velocities

## 1. Definitions

- **First Cosmic Velocity** (Orbital velocity):  
  The minimum velocity required for an object to achieve a stable circular orbit just above the surface of a celestial body.

  $$
  v_1 = \sqrt{\frac{GM}{R}}
  $$

- **Second Cosmic Velocity** (Escape velocity):  
  The minimum velocity needed to completely escape the gravitational pull of a celestial body without further propulsion.

  $$
  v_2 = \sqrt{2} \times v_1 = \sqrt{\frac{2GM}{R}}
  $$

- **Third Cosmic Velocity** (Solar system escape velocity):  
  The velocity needed to escape not just the Earth but also the Sun's gravitational pull from Earth's orbit.

---

## 2. Mathematical Derivations

- From Newton's Law of Gravitation:

  $$
  F = \frac{GMm}{r^2}
  $$

  Equating gravitational force to centripetal force for circular motion:

  $$
  \frac{mv^2}{r} = \frac{GMm}{r^2}
  $$

  Solving for $v$:

  $$
  v = \sqrt{\frac{GM}{r}}
  $$

  This gives the **first cosmic velocity**.

- For **escape velocity**, we equate kinetic energy to gravitational potential energy:

  $$
  \frac{1}{2}mv^2 = \frac{GMm}{r}
  $$

  Solving for $v$:

  $$
  v = \sqrt{\frac{2GM}{r}}
  $$

  This is the **second cosmic velocity**.

- The **third cosmic velocity** involves the escape from the solar system, considering the Earth's orbital speed around the Sun.

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

## 4. Results

The calculated cosmic velocities for Earth, Mars, and Jupiter are summarized below:

\[
\begin{array}{|c|c|c|}
\hline
\textbf{Celestial Body} & \textbf{First Cosmic Velocity (km/s)} & \textbf{Second Cosmic Velocity (km/s)} \\
\hline
\text{Earth} & 7.91 & 11.18 \\
\hline
\text{Mars} & 3.55 & 5.02 \\
\hline
\text{Jupiter} & 42.08 & 59.49 \\
\hline
\end{array}
\]

- **First Cosmic Velocity**: The minimum speed needed for a stable circular orbit near the surface.
- **Second Cosmic Velocity**: The minimum speed needed to escape the gravitational influence completely.
