
- **Problem definition** 
- **Why the state-of-the-art is not enough for this? Why does it fail?**
- **What is the clever idea of this paper?** 
- **How the idea is implemented? (algorithm, network structure, system...)** 
- **How is success proved and measured? (experiments, metrics, most relevant result)**

g(o) : O -> A
Observation to Action

f(a) : A -> u
Action to Control Input

u = f ◦ g(o)
Observation to Control Input Through Action

## Problem Definition
Different tasks can be successfully achieved by different action spaces. However, robotic manipulation in RL has focused on the observation space or reward model rather than action space, despite appropriate action space can simplify the exploration and improve robustness.  Therefore, the author points out challenges of time-varying task constraint of compliance in contact-rich robotic manipulation tasks and investigates the effect of action space choice with variable stiffness in the performance of deep RL.

## Why the state-of-the-art is not enough for this? Why does it fail?
The performance of VICES depends on the robot modeling of kinematics and dynamics. Learning variable impedance control may not execute exception handling well. 

## What is the clever idea of this paper?
This method compensates for both kinematics and dynamics, which enable generalization of the task across different robots. 

## How the idea is implemented? (algorithm, network structure, system...)
Policies are trained using reinforcement learning to output actions on different action spaces. It predicts both end-effector displacement (reference) and variable impedance gains based on observations. It compares common choices for the action space in contact-rich manipulation and evaluates different action spaces.

## How is success proved and measured? (experiments, metrics, most relevant result)
The experiments evaluate sample efficiency, task completion, energy consumption, task success, and transferability between robots. Learned policies to perform tasks such as path following in free space, door opening, and table wiping in simulation and real robot (wiping) to demonstrate the effectiveness of VICES.