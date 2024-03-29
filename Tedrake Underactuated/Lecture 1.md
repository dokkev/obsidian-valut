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
![[Pasted image 20240304134016.png]]

$\ddot{q}$ would be joint acceleration

This is a specific version. We can write in more general form:

$$
X = 
\begin{bmatrix}
q \\ 
\dot{q}
\end{bmatrix}
$$
$$
\dot{X} = f(x,u) = 
\begin{bmatrix}
\dot{q} \\
f(q,\dot{q},u)
\end{bmatrix}
$$

We can be more specific: "control affine" nonlinear system
![[Pasted image 20240304134815.png]]

This system is fully-actuated in the state $q, \dot{q}$ if only if $f_2(q,\dot{q})$ is full row rank.

#### Linear Algebra Review: 
- Rank is the number of dimension in the output of transformation
- Set of all possible output $A\vec{v}$ is called column space
- If the rank equals the number of the column, the matrix is **full rank**

![[Pasted image 20240304160851.png]]

The system is under-actuated if rank($f_2(q,\dot{q})) < dim(q)$  
For many systems, these hold for all $q,  \dot{q}$ -> system is underactuated.

#### Feedback Equivalence
![[Pasted image 20240304161304.png]]

As long as the inverse of $f_2$ exists → $\ddot{q} = \ddot{q}^d$ 

#### Manipulator Equation  
$$
M(q)\dot{q} + C(q,\dot{q})\dot{q} = \tau(g) + Bu
$$
- There is one exception with quaternion for Coriolis term
- $M(q) > 0$ : Mass matrix is positive definite
	- The Mass matrix is invertible
	- ![[Pasted image 20240304165853.png]]

