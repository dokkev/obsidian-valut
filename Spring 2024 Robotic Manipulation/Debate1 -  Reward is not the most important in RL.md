
## Key Concepts
- Exploitation:  a greedy approach in which agents try to get more rewards by using estimated value but not the actual value
-  Exploration: agents primarily focus on improving their knowledge about each action instead of getting more rewards so that they can get long-term benefits.

## Arguments
- My argument is reward function is not the most important aspect in training a control  policy by reinforcement learning.
- Rather, I argue that State and algorithm are more important. 
- Reinforcement Learning process includes an agent takes an action which affects the environment, and the environments gives reward and provides state to the agent.
- But in reality, there are more layers when it comes to deploying policy trained from RL to a real robot.
- Action goes into control input, which usually consists of high level controller and low level controller. 
- Then the robot physically interacts with the environment with uncertainty, and the sensors collect information from the environment, which also involves uncertainty.
- Due to these uncertainty, there is large gap between 