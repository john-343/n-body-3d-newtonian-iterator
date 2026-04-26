# n-body-3d-newtonian-iterator
A real-time interactive **N-body gravitational simulation** implemented in JavaScript using Three.js and Newtonian mechanics.

I made this iterator back around 2018 under the guidance of Dr. Taicheng Ouyang, who had asked me to create a html/js version of a previously existing java iterator. Though I was able to directly translate some features into javascript, I ended up needing to write many parts from scratch to attain the same features as the java version. I decided to finally get my code public again after many years, hence the outdated three.js version. 


## How to Use:
Here is a sample initial condition (from Ouyang's research)
0.01 100
5.8166 0 0 0.0001 0.3803 0.0000 10.0000
-9.5168 0.0008 -0.1376 0.1547 -0.8752 0.2103 5.0000
-10.5825 -0.0041 0.6879 -0.7740 0.5729 -1.0517 1.0000

initial coditions follow this template:

Header:

dt g   

(this is step size and strength of gravity. Default is .01 and 100)

Each body gets a row of 7 values:

x y z vx vy vz m

which represents a 3d position, a 3d vector (velocity), and finally the mass of the body.





## Overview

This short project simulates only gravitational interactions between bodies; no other forces are included. This was mant for the purpose of testing orbits for stability in 2018, so it is a bit old, hence some of the old js libraries. I may update for smoother run time, prettier graphics, additional functions in the future, but I mainly wanted to save my work onto something accessible for now.




## Physics Model

The simulation is based entirely on Newtonian gravity:

\[
F = G \frac{m_1 m_2}{r^2}
\]

Each body interacts with each other body pair-wise. The system is solved using explicit Euler integration:

- Velocity update:  
  v(t + dt) = v(t) + a(t) · dt

- Position update:  
  x(t + dt) = x(t) + v(t) · dt



## Current Features

- N-body gravitational simulation (any number of bodies)
- Real-time 3D rendering using Three.js
- Adjustable initial conditions via input field
- Camera controls (very janky right now)
- Center-of-mass tracking
- Trajectory visualization



## Controls

- Arrow keys:
  - ↑ / ↓ : zoom in/out
  - ← / → : adjust simulation speed

- WASD:
  - camera movement (good luck)

- Buttons:
  - Start/Pause simulation
  - Change focus object
  - Reset camera
  - Save system state - outputs a copy/paste-able list of current masses, positions and velocity.



## Notes

- Pure Newtonian gravity only
- Deterministic chaotic system (sensitive to initial conditions)
- Performance scales as O(n²)


