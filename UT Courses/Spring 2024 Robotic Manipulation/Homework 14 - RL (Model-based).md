# Model-based and Model-free RL for Robot Control
## Problem Definition
Dynamic programming suffers from practical challenges such as the curse of dimensionality and performance in unknown environments. Therefore, the author introduces reinforcement learning, which can solve a more general problem optimally within an unknown environment. 

## Summary of the methodology presented: algorithm, input-output
RL includes a system with its state and control input for the system, and the environment has a reward function which defines the reward associated with every state and control. The RL algorithm aims to accumulate the highest possible reward. Model-based RL uses am explicit model of the environment's dynamics, while model-free RL solely learns by interacting with the environment with reward. Deep reinforcement learning incorporates neural networks.

## Applicability / Problems solved
RL is very useful to synthesize optimal or robust policy in the unknown environment. Especially, some tasks involving multi-contact which suffers from difficulties and costliness of precise modeling can be solved with RL. In addition, RL is highly adaptable to changes in the environment that it can provide robust policy strong again perturbations 

## Assumptions and limitations
RL assumes that a given reward function accurately represents the successfulness of the desired tasks. If the tasks' reward function is hard to be defined, RL will not provide a viable solution. Moreover, RL assumes an explicit relationship of cause and effect (action and reward) which may not be the case for actions with long-term consequence. 