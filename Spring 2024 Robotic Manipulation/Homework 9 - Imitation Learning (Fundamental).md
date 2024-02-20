CS237B Lecture 12: Imitation Learning

## Problem Definition
While it assumes that the reward function is known in robot learning, Reinforcement Learning suffer from setting appropriate reward function and getting potentially sparse reward. This results in the learning process expensive in amount of data n and time needed while exploring with sub-optimal policy.
## Summary of the methodology presented: algorithm, input-output
The author introduces two classical imitation learning, which are behavior cloning (BC) and DAgger, and he shows approaches for learning the reward function referred as Inverse Reinforcement Learning (IRL).  BC takes an expert's demonstration as input and outputs a policy which replicates the demonstration. DAgger expands from BC and aims to improve the policy by incorporating feedback from the expert. Finally, IRL aims to find the reward function from the demonstration.
## Applicability / Problems solved
Imitation learning is useful where defining reward function is challenging or when an expert can demonstrate the problem-solving. It solves complex decision-making process such as robotic manipulation task requires several sub-tasks and requirement for extensive exploration during training robot learning policies.
## Assumptions and limitations

BC works under the assumption that the expert can cover the state space and provide sufficient data to the robot through the demonstration. In addition, DAgger assumes that the expert can provide feedback on new state. The robustness of the policy will depend on both quantity and quality of demonstration from the expert. Therefore, task generalization through imitation learning becomes very expensive. 