## Integrated Task and Motion Planning (TAMP) in robotics

## Problem Definition
The author addresses challenges of translating abstract plans defined in PDDL into feasible actions in the real world where obstacles and hardware limitation exists. This involves not only deciding the sequence of actions, but also ensuring these actions can be achieved physically by the robot in the given environment. 

## Summary of the methodology presented: algorithm, input-output
TAMP incorporates both task and motion planning into a combined framework which requires more upfront computation but provides safer robot behaviors. In detail, hierarchical planning techniques and sampling-based strategies are combined to accept high level goals, environments, and robot state as inputs and to output a sequence of actions and specific motions to achieve desired goals.

## Applicability / Problems solved
TAMP is capable of performing tasks in complex environments with obstacles, such as determining if a path or action is feasible and manipulating objects with collision avoidance. Also, it can reduce the risk of plan failure by incorporating detailed deliberation on the feasibility of plans.
## Assumptions and limitations
The author assumes that the enviroment can be accuratly modeled with a planning launguage such PDDL
