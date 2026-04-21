# n-body-3d-newtonian-iterator

A real-time interactive **N-body gravitational simulation** implemented in JavaScript using Three.js and Newtonian mechanics.

---

## 🌌 Overview

This project simulates the gravitational interaction of **N bodies** in three-dimensional space using classical Newtonian physics. Each body interacts with every other body via pairwise gravitational forces.

The system evolves over time using a numerical integration approach (explicit Euler method).

---

## ⚙️ Physics Model

The simulation is based entirely on Newtonian gravity:

\[
F = G \frac{m_1 m_2}{r^2}
\]

Each body experiences the net gravitational force from all other bodies in the system.

No relativistic effects, dark matter models, or cosmological expansion terms are included.

---

## 🧮 Numerical Method

The system is solved using **explicit Euler integration**:

- Velocity update:  
  v(t + dt) = v(t) + a(t) · dt

- Position update:  
  x(t + dt) = x(t) + v(t) · dt

---

## 🧪 Features

- N-body gravitational simulation (any number of bodies)
- Real-time 3D rendering using Three.js
- Adjustable initial conditions via input field
- Camera controls (free movement + focus modes)
- Center-of-mass tracking
- Trajectory visualization

---

## 🎮 Controls

- Arrow keys:
  - ↑ / ↓ : zoom in/out
  - ← / → : adjust simulation speed

- WASD:
  - camera movement (free mode)

- Buttons:
  - Start/Pause simulation
  - Change focus object
  - Reset camera
  - Save system state

---

## 🧠 Notes

- Pure Newtonian gravity only
- Deterministic chaotic system (sensitive to initial conditions)
- Performance scales as O(n²)


