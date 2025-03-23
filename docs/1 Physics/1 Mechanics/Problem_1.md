# Problem 1
# Investigating the Range as a Function of the Angle of Projection

## Motivation

Projectile motion, while seemingly simple, offers a rich playground for exploring fundamental principles of physics. The problem is straightforward: analyze how the range of a projectile depends on its angle of projection. Yet, beneath this simplicity lies a complex and versatile framework.

What makes this topic particularly compelling is the number of free parameters involved in these equations, such as initial velocity, gravitational acceleration, and launch height. These parameters give rise to a diverse set of solutions that can describe a wide array of real-world phenomena, from the arc of a soccer ball to the trajectory of a rocket.

---

## 1. Theoretical Foundation

Assume a projectile is launched with initial speed `v₀` at an angle `θ` from the horizontal.

The horizontal and vertical components of the velocity are:

```
v₀ₓ = v₀ * cos(θ)
v₀ᵧ = v₀ * sin(θ)
```

Using the kinematic equations:

- Horizontal displacement:

```
x(t) = v₀ * cos(θ) * t
```

- Vertical displacement:

```
y(t) = v₀ * sin(θ) * t - (1/2) * g * t²
```

Time of flight `T` (when `y(T) = 0`):

```
T = (2 * v₀ * sin(θ)) / g
```

The range `R` is:

```
R = v₀ * cos(θ) * T = (v₀² * sin(2θ)) / g
```

---

## 2. Analysis of the Range

From the formula:

```
R(θ) = (v₀² * sin(2θ)) / g
```

- Range is maximized when `θ = 45°` (since `sin(2θ) = 1`)
- Symmetric about `45°`: `R(θ) = R(90° - θ)`
- Increases with `v₀²`, decreases with `g`

### Parametric Sensitivity

- **Initial Velocity (`v₀`)**: A doubling of `v₀` increases the range by a factor of 4.
- **Gravitational Acceleration (`g`)**: Stronger gravity reduces the range.
- **Angle of Projection (`θ`)**: Maximum range at `45°` on flat ground.

---

## 3. Practical Applications

The ideal model assumes:
- Flat launch and landing height.
- No air resistance.
- Constant gravity.

**Real-world adaptations include:**
- Uneven terrain: requires solving for different launch and landing heights.
- Air resistance: introduces drag force `F_d = -kv`, complicating equations.
- Wind: affects horizontal acceleration.
- Variable gravity: in astrophysical or orbital contexts.

---

## 4. Python Implementation

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters
v0 = 30  # initial velocity in m/s
g = 9.81  # gravity in m/s^2
angles = np.linspace(0, 90, 500)  # angle in degrees
theta_rad = np.radians(angles)

# Compute range
R = (v0**2) * np.sin(2 * theta_rad) / g

# Plot
plt.figure(figsize=(8, 5))
plt.plot(angles, R)
plt.title("Projectile Range vs. Launch Angle")
plt.xlabel("Angle (degrees)")
plt.ylabel("Range (meters)")
plt.grid(True)
plt.show()
```

---

## 5. Limitations and Further Improvements

- **Drag forces**: Requires numerical modeling with differential equations.
- **Wind effects**: Adds to complexity in horizontal motion.
- **3D trajectory**: Needed for real sports or ballistic applications.
- **Variable terrain**: Involves elevation maps or terrain functions.

---

## Conclusion

This project explores how the range of a projectile is influenced by launch angle, velocity, and gravity. While the basic model is elegant and useful, its real-world application benefits from enhancements like drag and terrain modeling.
