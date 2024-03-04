Null-space control in robotics is an advanced control strategy that leverages the mathematical concept of the null space of a matrix to achieve secondary objectives without affecting the primary task of a robot. 

This concept is particularly useful in robotic systems with redundant degrees of freedom (DOF), where the robot has more DOFs than are strictly necessary to perform a given task. 

The redundancy allows the robot to optimize secondary criteria, such as avoiding obstacles, minimizing energy consumption, or optimizing the robot's posture, while still accomplishing the primary task.

In robotics, the primary task of an end-effector can be written in 
$$
\dot{x} = J\dot{q}
$$
When the robot is redundant, Jacobian has non-trivial null space meaning there exist non-zero vectors $z$ such that $Jz = 0$. These $z$ do not affect the end-effector's position or velocity.

The general solution $
\dot{x} = J\dot{q}
$
