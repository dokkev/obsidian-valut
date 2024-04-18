Operational Space 는 로봇이 실제 작업을 수행하는 공간을 의미
가끔식 Task Space 라고 불리기도 함.
-> End-effector 가 Task Space 에서 원하는 pose 에 도달하거나 특정 Force 를 출력하고자 할 때, 필요한 Torque 는 얼마인가?

Object in Task Space is described using SE(3) and SO(3). 

### Work and Power

$$
W = \int{F^{T}v *dt} = F^{T} d
$$
$$ P = \frac{W}{t} = \frac{F^Td}{t}= F^{T}v$$
In joint space, $q$
$$P_q = F^T_q*\dot{q}$$
In task space, $X$:
$$P_{X}= F^T_X*\dot{X}$$
By conservation of energy,
$$
P_{q}= P_{X} => F^{T}_{q} \dot{q} = F^{T}_{X} \dot{X} 
$$

### Dynamics Model

By Jacobian,
$$\dot{X} = J(q)\dot{q} $$
Substituting:
$$
F^{T}_{q} \dot{q} = F^{T}_{X} * J(q)\dot{q}
$$
$$
F_{q}= J^T(q)F_X
$$
By Newton's 2nd Law:
$$
F_{X}= M_X*\ddot{X}
$$
Let's say that control input (joint torque), $u \equiv F_q$

$$
u = J^T(q)M_X\ddot{X}_d
$$
Where $M_X$ is inertia matrix in task space (6 x 6) and $\ddot{X_d}$ is desired acceleration.

This equation explains how much control input (joint torque) is needed to generate desired acceleration in the task space.

Let's look at the robot dynamics model in joint space using spring-damper model

$$
M_{q}\ddot{q}= u - C(q,\dot{q}) - g(q)
$$
Where $C$ term is Coriolis effect and Centrifugal force while $g$ represents gravity term. $M_q$ is a mass matrix in joint space. In 7-dof robot manipulator with (7 x 7) dimension.

Rewriting:
$$
\ddot{q} = M_{q}^{-1} (u - C(q,\dot{q} - g(q)) 
$$
Let's go back to the Task space velocity representation.
$$\dot{X} = J(q)\dot{q}$$
by taking derivative in terms of time,
$$
\ddot{X} = \dot{J}(q)\dot{q} + J(q)\ddot{q}
$$
Substituting $\ddot{q}$ with joint space dynamics equation,
$$
\ddot{X} =  \dot{J}(q)\dot{q} + J(q) * M_{q}^{-1}[u - C(q,\dot{q}) - g(q)]
$$
$$$$
while $u = J^T(q)M_X\ddot{X}_d$  
$$
\ddot{X} =  \dot{J}(q)\dot{q} + J(q) * M_{q}^{-1}[J^T(q)M_X\ddot{X}_d - C(q,\dot{q}) - g(q)]
$$
We can simplify this by ignoring C, Jdot, and g:
$$
\ddot{X} = J(q)M_{q^{-1}}J^{T}(q)M_{X}\ddot{X_d}
$$

$$$$

