# Problem 3
# Trajectories of a Freely Released Payload Near Earth

## 1. Theoretical Background

When a payload is released from a moving spacecraft near Earth, its trajectory depends on:

- Initial position (altitude above Earth's surface),
- Initial velocity (magnitude and direction),
- Gravitational force acting toward Earth’s center.

The motion is governed by Newton’s Law of Universal Gravitation:

$$
F = \frac{G M m}{r^2}
$$

Where:

- $F$ is the gravitational force,
- $G = 6.67430 \times 10^{-11} \, \text{m}^3 \, \text{kg}^{-1} \, \text{s}^{-2}$ is the gravitational constant,
- $M$ is Earth's mass ($5.972 \times 10^{24} \, \text{kg}$),
- $m$ is the mass of the payload (cancels out),
- $r$ is the distance from Earth's center.

The equation of motion becomes:

$$
\ddot{r} = -\frac{G M}{r^3} r
$$

Depending on the energy:

- Elliptical trajectory if total energy $E < 0$,
- Parabolic trajectory if $E = 0$,
- Hyperbolic trajectory if $E > 0$.

Where total energy:

$$
E = \frac{1}{2} m v^2 - \frac{G M m}{r}
$$

Escape velocity at a given altitude:

$$
v_{\text{esc}} = \sqrt{\frac{2 G M}{r}}
$$

If $v < v_{\text{esc}}$: payload remains bound (orbit or reentry).

If $v \geq v_{\text{esc}}$: payload escapes Earth’s gravity.

---

## 2. Numerical Simulation Approach

We solve the second-order differential equation for motion numerically using time stepping (Euler or Runge-Kutta 4th order).

At each time step:

- Update acceleration based on current position.
- Update velocity based on acceleration.
- Update position based on velocity.

We assume:

- No atmospheric drag (valid at high altitudes).

---

## 3. Python Script

Below is the Python code that:

- Defines Earth parameters,
- Simulates the motion,
- Visualizes trajectories for different initial velocities.

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11  # gravitational constant, m^3/kg/s^2
M_earth = 5.972e24  # mass of Earth, kg
R_earth = 6371e3  # radius of Earth, meters

# Function to compute acceleration
def acceleration(r):
    r_norm = np.linalg.norm(r)
    return -G * M_earth * r / r_norm**3

# Runge-Kutta 4th order method
def rk4_step(r, v, dt):
    k1_v = acceleration(r)
    k1_r = v

    k2_v = acceleration(r + 0.5*dt*k1_r)
    k2_r = v + 0.5*dt*k1_v

    k3_v = acceleration(r + 0.5*dt*k2_r)
    k3_r = v + 0.5*dt*k2_v

    k4_v = acceleration(r + dt*k3_r)
    k4_r = v + dt*k3_v

    r_new = r + (dt/6)*(k1_r + 2*k2_r + 2*k3_r + k4_r)
    v_new = v + (dt/6)*(k1_v + 2*k2_v + 2*k3_v + k4_v)

    return r_new, v_new

# Simulation function
def simulate_trajectory(r0, v0, t_max, dt):
    r = r0.copy()
    v = v0.copy()
    positions = [r0]

    for _ in range(int(t_max/dt)):
        r, v = rk4_step(r, v, dt)
        positions.append(r)

        if np.linalg.norm(r) < R_earth:  # collision with Earth
            break

    return np.array(positions)

# Initial conditions
altitude = 400e3  # 400 km above Earth's surface
r0 = np.array([R_earth + altitude, 0])  # starting position
v_circular = np.sqrt(G * M_earth / (R_earth + altitude))  # circular orbital speed
v_escape = np.sqrt(2) * v_circular  # escape velocity at that altitude

# Different initial velocities
velocities = [
    0.5 * v_circular,
    v_circular,
    1.1 * v_circular,
    v_escape
]

# Plot trajectories
plt.figure(figsize=(8,8))
theta = np.linspace(0, 2*np.pi, 100)
earth = R_earth * np.array([np.cos(theta), np.sin(theta)])
plt.plot(earth[0], earth[1], 'k')  # Earth outline

for v0_mag in velocities:
    v0 = np.array([0, v0_mag])
    trajectory = simulate_trajectory(r0, v0, t_max=20000, dt=1)
    plt.plot(trajectory[:,0], trajectory[:,1], label=f'v0 = {v0_mag/1000:.1f} km/s')

plt.legend()
plt.xlabel('x (m)')
plt.ylabel('y (m)')
plt.title('Trajectories of Released Payloads')
plt.grid()
plt.axis('equal')
plt.show()
```
