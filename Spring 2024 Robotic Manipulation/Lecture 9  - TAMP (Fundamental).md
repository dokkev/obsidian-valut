## Why TAMP?
- Tackle longer horizon tasks
## Task Planning
 - model based and defined at a high-level of abstraction
	- Assume some level of prior knowledge
	- definitions are discrete
	- model provide approximation
 - comprised of states, objects, and actions
### PDDL (Planning Domain Definition Language)
- Parameters
	- ?r
	- ?loc1
	- ?loc2
- Preconditions
	- A robot must have the same name as ?r
	- A location must have the same as ?loc1
- Effects
	-  The robot will be now at ?loc2
	- The robot will no longer be at ?loc1
	
### Limitation of Task Planning
- Feasibility is not considered
- Optimality is hard to be achieved
- The real world is continuous

## TAMP
- Sampling Strategies - Early Commitment
- Sampling Strategies - Least Commitment (or Optimistic)
### Hierarchical Planning

