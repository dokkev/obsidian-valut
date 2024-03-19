## Problem Definition
With advancement of computers, actuators, and sensors, robotic system with complex hardware such as humanoid robots have been developed. However, existing simulators which do not engage physics engines lack of speed and accuracy for automatic controller design, which requires significant computational resources due to large amount of evaluations in numerical optimizations. Game-based physics engine tend to prioritize the stability of the simulation rather than accuracy of physics. 
 
## Summary of the methodology presented: algorithm, input-output
The author presents MuJoCo (multi-joint contact simulation) which can parallelly evaluate dynamical systems, always compute inverse dynamics, and include actuator dynamics. The equation of motion in continuous time consists of forward dynamics term, equality constraint term, and contact term with consideration of impulse.  Forward kinematics of rigid-bodies construct Jacobian matrices, and inertia matrix is computed with RNE. Equality constraint impulse and contact impulse are calculated based on the constraint of rigid body. The author introduces several solvers for the contact impulse and their trade-offs

## Applicability / Problems solved
MuJoCo can accurately represent complex robotic hardware such as tendon and linkage transmission in fast speed, and ability to accurately represent hardware in simulation reduces sim-to-real gap and helps to synthesize controller designs. MuJoCo physics engine can evaluate complex dynamic systems with multiple joints faster than other physics engine. 

## Assumptions and limitations
Although the paper includes comparison of evaluations with SD/FAST, it lacks of comparison to other simulators such as Bullet or ODE.