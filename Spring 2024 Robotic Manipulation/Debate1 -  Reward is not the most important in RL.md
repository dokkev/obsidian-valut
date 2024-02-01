
## Key Concepts
- Exploitation:  a greedy approach in which agents try to get more rewards by using estimated value but not the actual value
-  Exploration: agents primarily focus on improving their knowledge about each action instead of getting more rewards so that they can get long-term benefits.

## Arguments
- My argument is reward function is not the most important aspect in training a control  policy by reinforcement learning.
- Rather, I argue State representation is the most important tin RL based control
- Reinforcement Learning process includes an agent takes an action which affects the environment, and the environments gives reward and provides state to the agent.
- But in reality, there are more layers when it comes to deploying policy trained from RL to a real robot.
- Action goes into control input, which usually consists of high level controller and low level controller. 
- Then the robot physically interacts with the environment with uncertainty, and the sensors such as encoders, IMU, FT sensors, and camera collect information from the environment, which also involves uncertainty.
- Due to this uncertainty, there is a large gap between simulation and real robot environment in terms of estimating the state.
- Even with an appropriate reward function, the control policy will fail without ability to adapt to an uncertain environment. 
- The success of RL algorithm depends on the high quality and dense reward feedback, but specific reward function lacks of generalization
- related to that, Google Research scientist, Rishabh Agarwal demonstrated Meta Reward  Learning which successfully trained policy from binary reward: success and failure from complex input such as a natural language instruction.  (semantic parsing and maze solving)
- From the research of Dulac-Arnold called Challenges of Real-World Reinforcement Learning addresses that how the state space and the extraction of relevant features significantly impact the learning process. 
- In addition, it argues that poor representation can lead to inefficiencies or failures in learning, regardless of the reward structure
- In terms of transfer learning, a robust state representation enables the RL agent to generalize from its learning to new situations enhancing its performance across a wide range of tasks.
- A well-structured state that reduces redundancy and irrelevant information can lead to faster learning and lower computational requirement
- The scalability: RL algorithms to high-dimensional or continuous spaces is directly tied to how state information is represented and managed. Efficient state representations, such as those utilizing function approximation techniques (e.g., deep learning), are pivotal for tackling real-world problems that involve large state spaces.
- 