# Problem 1

#  Lorentz Force — Simulation & Theory

##  Introduction

The **Lorentz Force** is the fundamental force experienced by a charged particle in electric and magnetic fields:

$$
\mathbf{F} = q\mathbf{E} + q\mathbf{v} \times \mathbf{B}
$$

Where:
- $q$: charge (Coulombs)
- $\mathbf{E}$: electric field (V/m)
- $\mathbf{v}$: velocity vector (m/s)
- $\mathbf{B}$: magnetic field (Tesla)

> **Important:** In this project, we simulate a macroscopic particle with  
> $q = 1~\text{C}$ and $m = 1~\text{g} = 10^{-3}~\text{kg}$  
> instead of tiny electron values to ensure visible and meaningful trajectories.

---

##  Useful Concepts & Formulas

### 1. Magnetic Force Only (no electric field)
$$
\mathbf{F} = q\mathbf{v} \times \mathbf{B}
$$
- Direction: Perpendicular to both $\mathbf{v}$ and $\mathbf{B}$
- Result: **Circular** or **helical** motion

### 2. Larmor Radius
$$
r_L = \frac{mv_\perp}{|q|B}
$$

### 3. Cyclotron Frequency
$$
\omega_c = \frac{|q|B}{m}
$$

### 4. E × B Drift Velocity
$$
\mathbf{v}_d = \frac{\mathbf{E} \times \mathbf{B}}{B^2}
$$

---

##  Example Problem

### **Circular Trajectory**

**Given:**
- $q = 1~\text{C}$, $m = 10^{-3}~\text{kg}$
- $v_\perp = 1~\text{m/s}$, $B = 1~\text{T}$

**Solution:**

1. Larmor Radius:
$$
r_L = \frac{10^{-3} \cdot 1}{1 \cdot 1} = 10^{-3}~\text{m}
$$

2. Cyclotron Frequency:
$$
\omega_c = \frac{1 \cdot 1}{10^{-3}} = 1000~\text{rad/s}
$$

---

##  Simulated Scenarios

| Scenario        | Initial Conditions                                      | Expected Motion        |
|------------------|----------------------------------------------------------|--------------------------|
| **Circular**     | $\mathbf{v} \perp \mathbf{B}$ only                      | Particle loops in plane |
| **Spiral in $z$**| $\mathbf{v}$ has $v_z$ component, $\mathbf{B} = B_z$   | Helix around $z$-axis   |
| **Drift Motion** | $\mathbf{E} \perp \mathbf{B}$                          | Uniform drift           |

Visualizations for each are in the [simulation notebook](../notebooks/lorentz_simulation.ipynb).

---

## 💬 Hints

- Use larger $q$ and $m$ for macroscopic scale motion
- Start with circular motion
- Introduce axial velocity for helices
- Add electric field for drift behavior
