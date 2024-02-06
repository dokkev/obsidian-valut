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
- Google map, sequential decision-making
- Graph Traversal Algorithms
- Breath-First Search (FIFO) → finds the shortest path
- Depth-First Search (LIFO) 
- Greedy Best First Search
	- picks the best, heuristic
- Astar combines BFS and GFS
	- optimal and fast
	- At each iternation, A chooses to explore the node of the frontier that minimizes the N (steps from the source to node + approximate steps to target)
- Dijkstra's Algorithm
- Completeness
	- If there is a solution, it will find it (with time < t), or return that there is no solution
- Optimality
	- Always finds the shortest path
- cs standfod abisee
- Curse of dimensionality
	- the complexity of the algorithm increases

## Sampling-based method
- PRM (Probabilistic Roadmap)
- RRT
	- 