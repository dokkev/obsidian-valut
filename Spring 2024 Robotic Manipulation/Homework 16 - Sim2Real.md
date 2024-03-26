## In-Hand Object Rotation via Rapid Motor Adaptation

## Problem Definition
Compared to human's ability to manipulate different objects in-hand, generalized in-hand manipulation to robot has been an unsolved challenge. Traditional method has demonstrated in-hand manipulation of limited objects using multi-fingered hands, highlighting the complexity of generalized robotic in-hand manipulation.

## Why the state-of-the-art is not enough for this? Why does it fail?

## What is the clever idea of this paper?

## How the idea is implemented
The controller is trained using reinforcement (PPO) in a simulated environment to learn the representation of the objects' extrinsic parameters and optimize the joint control policy. The base policy is trained with The policy infers a low-dimensional embedding of object’s properties such as size and mass from revision joint angles and action history, which is then used by our base policy to rotate the object.

##  How is success proved and measured?
