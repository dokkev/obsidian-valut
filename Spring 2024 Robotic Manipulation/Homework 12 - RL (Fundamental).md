# Markov Decision Processes, Intro to RL
## Problem Definition
Challenges in Robotic decision-making address that sequences of decisions must be made and uncertainty may exist in the environment. . The deterministic approach assumes a known outcome for each action, while the stochastic method accounts for uncertainty in outcomes, using probabilities to model various possible future states​​.
## Summary of the methodology presented: algorithm, input-output
**Deterministic DP** involves a sequence of decisions, modeled as a discrete-time system where the state transition depends on the current state and action. The objective is to minimize a cost function over a finite planning horizon. This approach uses backward recursion and the principle of optimality to compute the optimal control sequence​​. **Stochastic DP** extends this by incorporating uncertainty into the decision-making process through a stochastic model. The algorithm calculates policies that minimize the expected cost, considering random disturbances that affect state transitions. Input to these algorithms includes the system model, admissible controls, and a cost function, while the output comprises optimal policies or control sequences for navigating the state space​​.
## Applicability / Problems solved
This is applicable to a wide range of decision-making problems under uncertainty, such as frontier exploration. These methods provide a structured way to determine optimal sequences of actions in complex environments where future conditions may be uncertain or only partially known​​.

## Assumptions and limitations

