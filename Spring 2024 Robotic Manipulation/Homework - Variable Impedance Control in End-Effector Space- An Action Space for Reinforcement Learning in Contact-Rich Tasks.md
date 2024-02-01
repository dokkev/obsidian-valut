
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
Different tasks can be successfully achieved by different action spaces. However, robotic manipulation in RL has focused on the observation space or reward model rather than action space, despite appropriate action space can simplify the exploration and improve robustness.  Therefore, the author investigates the effect of action space choice in the performance of deep RL.

Why the state-of-the-art is not enough for this? Why does it fail?
