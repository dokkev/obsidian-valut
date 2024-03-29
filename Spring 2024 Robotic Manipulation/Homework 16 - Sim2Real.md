## In-Hand Object Rotation via Rapid Motor Adaptation

## Problem Definition
Compared to human's ability to manipulate different objects in-hand, generalized in-hand manipulation to robot has been an unsolved challenge. Traditional method has demonstrated in-hand manipulation of limited objects using multi-fingered hands, highlighting the complexity of generalized robotic in-hand manipulation.

## Why the state-of-the-art is not enough for this? Why does it fail?
While this paper only demonstrates rotation in one axis, the dexterous-manipulation task requires movement in SO(3). Since the policy only relies on proprioceptive information, the action is purely feed-forward, which is vulnerable to uncertainty and errors.  

## What is the clever idea of this paper?
This method consists of two parts: base policy and adaptation module training, and this provides robustness when deploying to real world compared to end-to-end policy. This method does not rely on sensors such as cameras or force/torque sensors, and the controller can be deployed without fine-tuning. 

## How the idea is implemented
The controller is trained using reinforcement (PPO) in a simulated environment to learn the representation of the objects' extrinsic parameters and optimize the joint control policy. 
The base policy is trained with object properties. Then the adaptation module is trained to infer a low-dimensional embedding of the object’s properties such as size and mass from revision joint angles and action history, which is then used by the base policy to rotate the object.

##  How is success proved and measured?
The policy is tested with both simulated and real-robotic hand (16 DOF) and compared to the baseline policies over 30 diverse objects. The metrics of evaluations are: rotations, time to fall, and energy efficiency. 
