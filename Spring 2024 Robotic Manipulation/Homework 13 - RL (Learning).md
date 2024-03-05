# End-to-End Training of Deep Visuomotor Policies

## Problem Definition
Designing the perception and control software for autonomous operation is challenging. While DNN with large amout of data and direction supervision shows successful applications in computer vision and speech recognition, it is hard to apply to robotic control due to real-world constraints. 
## Why the state-of-the-art is not enough for this? Why does it fail?

## What is the clever idea of this paper?
The authors combine perception system and control policy, which does not require full state information of the object.

## How the idea is implemented
The pose estimation is pretrained using dataset of camera images of varied positions of objects in the scene, and linear-Gaussian controller is pretrained with full state information for tasks under various initial states. involving trajectory-centric reinforcement learning 

##  How is success proved and measured?
