# n-body-3d-newtonian-iterator
A real-time interactive **N-body gravitational simulation** implemented in JavaScript using Three.js and Newtonian mechanics.

I made this iterator back around 2018 under the guidance of Dr. Taicheng Ouyang, who had asked me to create a html/js version of a previously existing java iterator. Though I was able to directly translate some features into javascript, I ended up needing to write many parts from scratch to attain the same features as the java version. I decided to finally get my code public again after many years, hence the outdated three.js version. 

---
## How to Use:
Here is a sample initial condition (from Ouyang's research)
0.01 100
5.8166 0 0 0.0001 0.3803 0.0000 10.0000
-9.5168 0.0008 -0.1376 0.1547 -0.8752 0.2103 5.0000
-10.5825 -0.0041 0.6879 -0.7740 0.5729 -1.0517 1.0000

initial coditions follow this template:

Header:
dt g   
this is step size and strength of gravity. Default is .01 and 100
Each body gets a row of 8 values:
x y z vx vy vz r m
which represents a 3d position, a 3d vector (velocity), the radius of the sphere representing the body, and finally the mass of the body.




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


