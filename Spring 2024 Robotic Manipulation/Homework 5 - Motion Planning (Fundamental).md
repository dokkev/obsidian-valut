## Problem Definition
Motion planning involves geometrically parametrizing the robot's state and its environment to synthesize its movement while avoiding collision. Although combinatorial solutions provided theoretical solutions, it was impractical due to computation limitation of high-dimensionality and complex configurations

## Summary of the methodology presented: algorithm, input-output
The configuration of the robot and obstacle in the environment can be represented as C-space, which represents all possible configuration of the robot. The motion planner takes the initial and desired goal position and outputs a collision-free path. The author presents combinatorial planning which captures all necessary information for planning and sampling-based planning which incrementally samples and searches for a path without characterizing all information of the environment.
## Applicability / Problems solved
Sampling-based motion planning such as RRTs is widely used in industries in both rigid 2D and 3D robots among fixed obstacles. 

## Assumptions and limitations
