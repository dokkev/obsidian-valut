## Goals for the class
- Bring together tools from
	- Nonlinear dynamics
	- Optimization
	- Control
	- Machine Learning
- Rigorous thinking about "model systems"
- Algorithmic toolkit for more complex systems

- Atlas is mostly -> online planning using with mechanics + optimization
- ANYmal / Quadrupeds → Reinforcement Learning
- Manipulation → Imitation Learning dominantly

These three things are inherently very similar.
- Optimization
	- Cost function / Imitating reference
- Vocab may be different

![[Pasted image 20240304132749.png]]

#### What makes control difficult?
- Uncertainty / Partial observation
- Actions have long-term consequences
- Nonlinearity and high-dimensionality (depends on)

#### Nonlinear Differential Equations
![[Pasted image 20240304133637.png]]
It is often referred to as "dynamic model".

![[Pasted image 20240304133729.png]]
And this is 'Observation model'

#### Linear Differential Equations
![[Pasted image 20240304133822.png]]


For mechanical systems:
Second order $F = ma$
