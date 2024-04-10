
## THE INGREDIENTS OF REAL-WORLD ROBOTIC REINFORCEMENT LEARNING
## Problem Definition
It is challenging to deploy autonomous learning robotic systems in real-world without episodic resets, which is a significant limitation o current robot learning algorithms. It is necessary for robots to learn from raw sensory inputs, self-assign rewards, and operate continuously in non-episodic setting to effectively collect real-world data for generalization

## Why the state-of-the-art is not enough for this? Why does it fail?

## What is the clever idea of this paper?

## How the idea is implemented
The idea is implemented through a combination of vision-based reinforcement learning (RL) using actor-critic algorithms, a vision-based goal classifier for rewards, and reset-free learning. The system employs variational inverse control with events (VICE) for reward specification and a variational autoencoder (VAE) for handling visual observations. This allows the robot to learn and adapt its behavior based on its sensory inputs and the outcomes of its actions, effectively navigating the complexities of real-world tasks without pre-programmed resets .
##  How is success proved and measured?
