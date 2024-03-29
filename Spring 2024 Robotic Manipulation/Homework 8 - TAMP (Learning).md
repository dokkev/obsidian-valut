
## Problem Definition
Language models lack real-world experience, which makes decision-making within a given embodiment challenging.  Since LLMs are not grounded in the physical world with no observation of the consequences of their generated actions, it can cause unsafe and unreasonable actions in physical worlds. Therefore, this limits for robots to leverage LLMs for decision-making process involving physical tasks in the real world.

## Why the state-of-the-art is not enough for this? Why does it fail?
SayCan works under the assumption of it has a good understanding of the environment of the robot state. It relies on the pre-defined skills and value functions, which may not be adaptable to dynamic environment in the real world. In addition, it may reflect the in accurate state of the environment, which can lead to inappropriate actions. The quality of generated actions of the robots are limited by the quality of pretrained skills of robots.
## What is the clever idea of this paper?
By combining, possible actions and feasibility, this method can be widely applied to robotics, where robots need to perform tasks with abstract and limited instructions. With its capability to translate a task into a sequence of sub-actions, SayCan can eliminate the necessity to set specific pre-defined actions for high-level task planning of tasks with similar characteristics (such as cutting apple vs cutting potato).

## How the idea is implemented
The author's method, SayCan is able to propose actions combined with semantic knowledge and robot's pretrained actions. As an input, it takes natural language instructions of a task for the robot. Then it interprets the task with LLM to generate possible actions to perform the task that the user provides, and it evaluates the feasibility of those actions with the pretrained robot skills. It selects the action based on the relevance and feasibility of the task.  As a result, it outputs a series of robot high level actions to execute the task and generate feedback for the next decision.
##  How is success proved and measured?
The SayCan system was evaluated in controlled environments (kitchen) using a mobile manipulator robot to perform a variety of tasks. The robot performed over 100 different instructions, grouped into various categories based on complexity, language structure, and the level of abstraction to test versatility and ability to handle instructions with varying degrees of specificity and complexity.
