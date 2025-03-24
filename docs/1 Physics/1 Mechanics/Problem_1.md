# Problem 1
# Investigating the Range as a Function of the Angle of Projection

## 1. Theoretical Foundation

### 1.1 Equations of Motion

Assuming an idealized system with no air resistance and where the projectile is launched from and lands at the same vertical level, the equations of motion can be derived from Newton’s laws: 

**Horizontal motion (constant velocity):**

$$
x(t) = v_0 \cos(\theta) \cdot t
$$

**Vertical motion (uniform acceleration):**

$$
y(t) = v_0 \sin(\theta) \cdot t - \frac{1}{2}gt^2
$$

Where:

- $v_0$ is the initial velocity  
- $\theta$ is the angle of projection  
- $g$ is the acceleration due to gravity  
- $t$ is time  

### 1.2 Time of Flight

To find the total time of flight $T$, set $y(T) = 0$:

$$
0 = v_0 \sin(\theta) \cdot T - \frac{1}{2}gT^2
$$

Solving for $T$:

$$
T = \frac{2v_0 \sin(\theta)}{g}
$$

### 1.3 Range

Substitute $T$ into the horizontal motion to find the range $R$:

$$
R = v_0 \cos(\theta) \cdot T = v_0 \cos(\theta) \cdot \frac{2v_0 \sin(\theta)}{g}
$$

Using the identity $\sin(2\theta) = 2 \sin(\theta) \cos(\theta)$:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

This is the key equation describing how the range depends on the angle of projection.

---

## 2. Analysis of the Range

### 2.1 Dependence on Angle

The range is maximized when $\sin(2\theta) = 1$, which occurs at:

$$
\theta = 45^\circ
$$

The graph of $R(\theta)$ is symmetric about $\theta = 45^\circ$, and the same range is achieved by complementary angles (e.g., $30^\circ$ and $60^\circ$).

### 2.2 Influence of Parameters

- **Initial velocity:** Since $R \propto v_0^2$, doubling the initial velocity quadruples the range.
- **Gravitational acceleration:** Since $R \propto \frac{1}{g}$, projectiles travel farther in weaker gravitational fields (e.g., on the Moon).

---

## 3. Practical Applications

### 3.1 Uneven Terrain

If launch and landing heights differ, the equations become more complex. For example, launching from height $h$, the vertical motion becomes:

$$
y(t) = h + v_0 \sin(\theta) \cdot t - \frac{1}{2}gt^2
$$

Solving for the time when $y(t) = 0$ gives a quadratic equation for $t$, and the solution can be used to compute the modified range.

### 3.2 Air Resistance and Wind

In realistic scenarios, air resistance introduces drag forces that depend on velocity (e.g., quadratic drag). These must be solved numerically, often using computational methods such as Euler's method or Runge-Kutta.

---

## 4. Implementation

Below is a Python script that simulates and visualizes the range as a function of projection angle:

```python
import numpy as np
import matplotlib.pyplot as plt

def compute_range(v0, g, angle_deg):
    theta = np.radians(angle_deg)
    return (v0**2 * np.sin(2 * theta)) / g

# Parameters
v0 = 20  # Initial velocity (m/s)
g = 9.81  # Gravitational acceleration (m/s^2)
angles = np.linspace(0, 90, 100)
ranges = compute_range(v0, g, angles)

# Plot
plt.figure(figsize=(10, 6))
plt.plot(angles, ranges)
plt.title('Projectile Range vs Angle of Projection')
plt.xlabel('Angle (degrees)')
plt.ylabel('Range (meters)')
plt.grid(True)
plt.show()

# --- Section 5: Limitations and Extensions ---

# Limitations:
# - The model assumes no air resistance (i.e., vacuum conditions).
# - Launch and landing heights are assumed to be equal.
# - No spin (Magnus effect) or wind is considered.

# Extensions:
# - Add air resistance using a velocity-dependent drag force and solve numerically.
# - Modify equations for projectiles launched from or landing on different elevations.
# - Introduce wind by including horizontal acceleration terms.
```
![alt text](image.png)

## My Colab (Canliy961)

[Projectile Range vs Angle of Projection](https://colab.research.google.com/drive/1zub6JQdK1DkVS4CyWHUYSn65Y6caYdtk?usp=sharing)
