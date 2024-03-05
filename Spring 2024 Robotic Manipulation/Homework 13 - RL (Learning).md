# End-to-End Training of Deep Visuomotor Policies

## Problem Definition
Designing the perception and control software for autonomous operation is challenging. While DNN with large amout of data and direction supervision shows successful applications in computer vision and speech recognition, it is hard to apply to robotic control due to real-world constraints. 
## Why the state-of-the-art is not enough for this? Why does it fail?
This method is highly dependent on initial state information, which may limit its applicability to other tasks. The performance of this policy will decrease if there is significant change in environment drifed from the training enviroment due to visual distractors 

## What is the clever idea of this paper?
The authors combine perception system and control policy, which does not require full state information of the object. This deep vasomotor policy addresses this issue by learning to map raw visual inputs to control actions in a unified framework.

## How the idea is implemented
The pose estimation is pretrained using dataset of camera images of varied positions of objects in the scene, and the linear-Gaussian controller is pretrained with full state information for tasks under various initial states involving trajectory-centric reinforcement learning. After successful pretraining, the vasomotor policy is trained by alternating between optimizing the trajectory distributions to minimize task-specific costs and optimizing the policy network to match these trajectories based on the observed camera images.

##  How is success proved and measured?
Success rates are directly measured by the policy's ability to accomplish the specified tasks under different condition to evaluate effectiveness and robustness of the policy. Tasks include hanging a coat hanger on a rack, inserting a block into a shape sorting cube, fitting a toy hammer under a nail, and screwing a cap onto a bottle, and these tasks are compared to two baseline methods.