# Problem 2
# Escape Velocities and Cosmic Velocities

## 1. Definitions

# Cosmic Velocities

### 1. First Cosmic Velocity (Orbital Velocity)

The first cosmic velocity is the minimum speed an object must have to stay in a stable circular orbit just above the surface of a planet, without falling back due to gravity.

To derive it:

The gravitational force provides the centripetal force needed for circular motion.

Gravitational force between a planet of mass $M$ and an object of mass $m$ is:

$$
F_{\text{gravity}} = \frac{G M m}{r^2}
$$

Centripetal force needed for circular motion is:

$$
F_{\text{centripetal}} = \frac{m v_1^2}{r}
$$

Setting gravitational force equal to centripetal force:

$$
\frac{G M m}{r^2} = \frac{m v_1^2}{r}
$$

Canceling $m$ from both sides and rearranging:

$$
v_1^2 = \frac{G M}{r}
$$

Taking the square root:

$$
v_1 = \sqrt{\frac{G M}{r}}
$$

Thus, the first cosmic velocity depends only on the mass of the planet and the radius at which the orbit occurs.

---

### 2. Second Cosmic Velocity (Escape Velocity)

The second cosmic velocity is the minimum speed needed for an object to completely escape the gravitational field of a planet, without any further propulsion.

To derive it:

The kinetic energy of the object must be enough to overcome the gravitational potential energy.

Kinetic energy:

$$
E_{\text{kinetic}} = \frac{1}{2} m v_2^2
$$

Gravitational potential energy at a distance $r$ from the center:

$$
E_{\text{potential}} = -\frac{G M m}{r}
$$

(negative because gravitational potential energy is zero at infinity and negative closer to the planet)

For escape, total energy must be zero:

$$
E_{\text{kinetic}} + E_{\text{potential}} = 0
$$

Substituting the expressions:

$$
\frac{1}{2} m v_2^2 - \frac{G M m}{r} = 0
$$

Rearranging:

$$
\frac{1}{2} m v_2^2 = \frac{G M m}{r}
$$

Canceling $m$ from both sides:

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

Thus, the second cosmic velocity is $\sqrt{2}$ times the first cosmic velocity:

$$
v_2 = \sqrt{2} \times v_1
$$

---

### 3. Third Cosmic Velocity (Solar System Escape Velocity)

The third cosmic velocity is the speed needed for an object not only to escape Earth's gravity, but also to escape the Sun's gravity from Earth's orbit.

To derive it:

When a spacecraft is launched from Earth, it already has Earth's orbital velocity around the Sun (about 30 km/s).

The spacecraft needs enough additional velocity to overcome the Sun’s gravitational pull.

The escape velocity from the Sun at Earth's orbit is found similarly:

Gravitational force by the Sun:

$$
F_{\text{sun}} = \frac{G M_{\text{sun}} m}{r_{\text{orbit}}^2}
$$

Escape velocity from the Sun at Earth's orbital radius:

$$
v_{\text{sun-escape}} = \sqrt{\frac{2 G M_{\text{sun}}}{r_{\text{orbit}}}}
$$

However, since Earth itself moves around the Sun at $v_{\text{Earth orbit}} \approx 30 \, \text{km/s}$, the spacecraft already has this velocity.

Thus, the spacecraft needs an extra boost:

$$
v_{\text{needed relative to Earth}} = v_{\text{sun-escape}} - v_{\text{Earth orbit}}
$$

In reality, because of orbital dynamics and energy considerations, the third cosmic velocity (starting from Earth's surface) turns out to be around **16.7 km/s**.

---

## Summary of Formulas

**First Cosmic Velocity:**

$$
v_1 = \sqrt{\frac{G M}{r}}
$$

**Second Cosmic Velocity:**

$$
v_2 = \sqrt{\frac{2 G M}{r}} = \sqrt{2} \times v_1
$$

**Third Cosmic Velocity (Approximate at Earth's distance from Sun):**

$$
v_3 \approx 16.7 \, \text{km/s}
$$

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
