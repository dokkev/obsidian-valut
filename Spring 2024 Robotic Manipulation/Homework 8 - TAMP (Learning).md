## Problem Definition
Language models lack real-world experience, which makes decision-making within a given embodiment challenging.  Since LLMs are not grounded in the physical world with no observation of the consequences of their generated actions, it can cause unsafe and unreasonable actions in physical worlds. Therefore, this limits for robots to leverage LLMs for decision-making process involving physical tasks in the real world.
## Summary of the methodology presented: algorithm, input-output
The author's method, SayCan is able to propose actions combined with semantic knowledge and robot's pretrained actions. As an input, it takes natural language instructions of a task for the robot. Then it interprets the task with LLM to generate possible actions to perform the task that the user provides, and it evaluates the feasibility of those actions with the pretrained robot skills. It selects the   As a result, it outputs a series of robot high level actions to execute the task

## Applicability / Problems solved

## Assumptions and limitations

