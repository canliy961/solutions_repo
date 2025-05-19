# Problem 1

# Simulating the Effects of the Lorentz Force

## 1. Exploration of Applications  
The Lorentz force governs the dynamics of charged particles in electric and magnetic fields:  
$F = q(\mathbf{E} + \mathbf{v} \times \mathbf{B})$

**Key Applications:**
- **Particle accelerators** (e.g., cyclotrons, synchrotrons): guide particles in circular paths using magnetic fields.  
- **Mass spectrometers**: use electric and magnetic fields to separate particles by mass-to-charge ratio.  
- **Plasma confinement**: magnetic fields trap and control plasma in fusion devices like tokamaks.  
- **Astrophysics**: cosmic rays spiral along interstellar magnetic field lines.

## 2. Simulating Particle Motion  
**Governing Equation:**  
We simulate particle motion using Newton’s 2nd law:  
$m \frac{d\mathbf{v}}{dt} = q(\mathbf{E} + \mathbf{v} \times \mathbf{B})$

Use Runge-Kutta (RK4) to solve this system numerically.

## 3. Python Code: Lorentz Force Simulation
```python
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D
 
# Constants
q = 1.0               # charge [C]
m = 1.0               # mass [kg] — increased to prevent blow-up
dt = 0.001            # smaller time step for better stability
steps = 20000          # number of steps
 
# Lorentz force equation
def lorentz_force(v, E, B):
    return q * (E + np.cross(v, B))
 
# Leapfrog (Velocity-Verlet) integration
def simulate_motion(v0, E, B, r0=np.array([0, 0, 0])):
    r = [r0]
    v = [v0]
   
    # First half-step velocity update (leapfrog)
    a = lorentz_force(v0, E, B) / m
    v_half = v0 + 0.5 * a * dt
 
    for _ in range(steps):
        # Full step position update
        r_next = r[-1] + v_half * dt
        r.append(r_next)
 
        # Compute acceleration at new position (based on velocity)
        a = lorentz_force(v_half, E, B) / m
 
        # Full step velocity update
        v_half = v_half + a * dt
        v.append(v_half - 0.5 * a * dt)  # Store full-step velocity for record
 
    return np.array(r), np.array(v)
 
# Fields and initial conditions
B = np.array([0, 0, 1])                 # Uniform magnetic field along z-axis
E = np.array([0, 0, 0])                 # No electric field
v0_spiral = np.array([1.0, 0.0, 0.5])   # Initial velocity with z-component
r0 = np.array([0.0, 0.0, 0.0])          # Starting at origin
 
# Run simulation
positions, velocities = simulate_motion(v0_spiral, E, B, r0)
 
# 3D Plot of the trajectory
fig = plt.figure(figsize=(8, 6))
ax = fig.add_subplot(111, projection='3d')
ax.plot(positions[:, 0], positions[:, 1], positions[:, 2])
ax.set_title("Stable Spiral Trajectory in Magnetic Field")
ax.set_xlabel("x")
ax.set_ylabel("y")
ax.set_zlabel("z")
plt.tight_layout()
plt.show()
```

![image](https://github.com/user-attachments/assets/fd38344d-9246-40b2-952d-1dad498f8d8b)

## 4. Parameter Exploration

**Field strengths ($\vec{E}$, $\vec{B}$):**  
Increasing magnetic field strength increases curvature (reduces Larmor radius).

**Initial velocity ($\vec{v}_0$):**  
Faster particles form larger spirals.

**Charge-to-mass ratio ($\frac{q}{m}$):**  
Heavier particles spiral less tightly.

### Characteristic Quantities

**Larmor Radius:**

$$
r_L = \frac{m v_\perp}{|q| B}
$$

**Cyclotron Frequency:**

$$
\omega_c = \frac{|q| B}{m}
$$

These quantities determine circular and spiral motion of particles in magnetic fields.

---

## 5. Physical Interpretation

### Case 1: Uniform Magnetic Field  
- Particle undergoes **circular or helical** motion.  
- If velocity has a component along the field direction, motion is **helical**.

### Case 2: Crossed Electric and Magnetic Fields  
- Particle experiences **$\vec{E} \times \vec{B}$ drift**:

$$
\vec{v}_{\text{drift}} = \frac{\vec{E} \times \vec{B}}{B^2}
$$

![image](https://github.com/user-attachments/assets/0b8dcbd3-6856-4651-bcc5-acb84a5f93b1)

![image](https://github.com/user-attachments/assets/efa7af53-7bfd-4005-89c8-92cc4a3a106e)

![image](https://github.com/user-attachments/assets/4c076add-759e-4f54-805f-d10cfdf1c548)

![image](https://github.com/user-attachments/assets/b9c081c9-de7a-4c1e-b95f-6072cef837b6)

![image](https://github.com/user-attachments/assets/989a3e08-db3c-4f2a-ac4a-bc208ec28183)

**Explanation:**  
The $\vec{E} \times \vec{B}$ drift velocity is given by:

$$
\vec{v}_{\text{drift}} = \frac{\vec{E} \times \vec{B}}{B^2}
$$

For $\vec{E} = [0, 10, 0]$ and $\vec{B} = [0, 0, 1]$, we get:

$$
\vec{v}_{\text{drift}} = \frac{[0, 10, 0] \times [0, 0, 1]}{1^2} = \frac{[10, 0, 0]}{1} = [10, 0, 0]
$$

The result is a circular or spiral motion in the plane, drifting steadily in the $x$-direction — a common effect in plasma physics and beam devices.


## My Colab (Canliy961)

[Lorentz Force](https://colab.research.google.com/drive/1DjZTBUMW_Lkngzsa6vyPxuFU_I6KVTIs#scrollTo=AWnZQk2UcWon)
