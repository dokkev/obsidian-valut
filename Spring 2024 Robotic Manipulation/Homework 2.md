### Fundamentals of Grasping
#### Problem definition (2-3 sentences)
Grasping is challenging due to its 
- High-dimensionality: multijoint robotic hand creates high DOF
- Complexity of contact: feasible contact is restricted by gripper's geometry
- Risk of collision: the entire body collision should be avoided.
- Evaluation: it requires to relatively evaluate the quality of the grasping.

#### Summary of the methodology presented: algorithm, input-output. (1-2 sentences)
The author introduces mathematical modeling of frictionless point contact, point contact with friction, soft-finger contact. The wrench matrix, which can be represented as individual applied finger force times grasp map, and it can be used to optimize the force applied and evaluate grasping
#### Applicability / Problems solved (2-3 sentences)
The method can apply to multi-contact in hand manipulation with capability to exert desired wrench to an object. It provides solution of evaluating grasping by tracking wrench.

#### Assumptions and limitations (1-2 sentences)
The method assumes the center of the mass of an object and desired wrench are known. It only addresses static friction model with rigid body object.