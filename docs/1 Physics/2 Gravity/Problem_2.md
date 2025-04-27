# Problem 2
# Escape Velocities and Cosmic Velocities

## 1. Definitions

### Cosmic Velocities

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

### Summary of Formulas

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

### 2.1 Derivation of the First Cosmic Velocity (Orbital Velocity)

The first cosmic velocity is the speed needed for an object to maintain a stable circular orbit just above the surface of a planet without falling back.

Start by considering the two forces:

**Gravitational force** acts to pull the object toward the center:

$$
F_{\text{gravity}} = \frac{G M m}{r^2}
$$

**Centripetal force** keeps the object moving in a circle:

$$
F_{\text{centripetal}} = \frac{m v_1^2}{r}
$$

To maintain a circular orbit, these two forces must balance:

$$
\frac{G M m}{r^2} = \frac{m v_1^2}{r}
$$

Simplify:

- Cancel $m$ from both sides.
- Multiply both sides by $r$.

Result:

$$
G M = v_1^2 r
$$

Solve for $v_1$:

$$
v_1^2 = \frac{G M}{r}
$$

Taking the square root:

$$
v_1 = \sqrt{\frac{G M}{r}}
$$

Thus, the first cosmic velocity is:

$$
v_1 = \sqrt{\frac{G M}{r}}
$$

---

### 2.2 Derivation of the Second Cosmic Velocity (Escape Velocity)

The second cosmic velocity is the minimum speed needed for an object to completely escape the gravitational field of a planet.

The idea is based on energy conservation: the object must have enough kinetic energy to overcome its gravitational potential energy.

Kinetic energy:

$$
E_{\text{kinetic}} = \frac{1}{2} m v_2^2
$$

Gravitational potential energy:

$$
E_{\text{potential}} = -\frac{G M m}{r}
$$

At the surface, the total mechanical energy must be zero for escape:

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

Multiply both sides by 2:

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

(meaning it is $\sqrt{2}$ times larger than the first cosmic velocity.)

---

### 2.3 Derivation of the Third Cosmic Velocity (Solar System Escape Velocity)

The third cosmic velocity is the speed needed not just to escape Earth’s gravity, but also the Sun's gravity from Earth’s orbit.

First, the escape velocity from the Sun at Earth's orbit is:

$$
v_{\text{sun-escape}} = \sqrt{\frac{2 G M_{\text{sun}}}{r_{\text{orbit}}}}
$$

Where:

- $M_{\text{sun}}$ is the mass of the Sun,
- $r_{\text{orbit}}$ is the distance from the Sun to the Earth (about 1 AU, or $1.496 \times 10^{11}$ meters).

However, the spacecraft already has Earth's orbital speed around the Sun, about 30 km/s.

Thus, the additional velocity needed is the difference:

$$
v_{\text{needed}} = v_{\text{sun-escape}} - v_{\text{Earth orbit}}
$$

In practice, considering Earth's own gravitational pull, atmosphere, and the need to overcome Earth's gravity first (second cosmic velocity), the real calculation is more complex.

When everything is accounted for, the third cosmic velocity from the Earth's surface is approximately **16.7 km/s**.

---

### Quick Recap

| Cosmic Velocity         | Meaning                              | Formula |
|--------------------------|--------------------------------------|---------|
| First Cosmic Velocity    | Orbital velocity around Earth        | $v_1 = \sqrt{\frac{G M}{r}}$ |
| Second Cosmic Velocity   | Escape Earth’s gravity               | $v_2 = \sqrt{2} \times v_1 = \sqrt{\frac{2 G M}{r}}$ |
| Third Cosmic Velocity    | Escape Sun’s gravity from Earth's orbit | Approx. 16.7 km/s |

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
