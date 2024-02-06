## What is motion planning
- way to A to B without collision
- Searching path in C-space consists of Cartesian space  which made of joint spaces
- Take a look at Configuration Space Visualization of 2-D Robotic manipulator (cs.unc.edu)
	- Two joint angles are represented as x-y plane
- Two families of solutions
	- Combinatorial (Graph search) methods
	- Sampling based methods
## Graph Search Method
- Transform the problem of finding a path as a problem to find a connection between two nodes in a graph
- Discretize the problem → construct graph → find a path
- Google map, sequential desicion making