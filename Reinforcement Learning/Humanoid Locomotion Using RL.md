강화학습에서의 평가/성능 지표
- Robustness
	- external force
	- ground variation
- Better performance
	- velocity tracking
	- faster motion

Opinion:
- Measuring robustness can be challenging. 
- Performance evaluation is challenging as well because it requires setting up different simulation environment. If commercial, the company may provide controllers (integrated into the robot)


## Reinforcement Learning Basics

![[rl_framework.png|500]]


RL environment involves an Agent and Environment. The Agent takes action based on the State, and the Environment provides next State and Reward to the Agent.

![[reward_eq.png]]

The goal is to maximize the accumulative reward over instantaneous reward. Gamma is a discount factor which reflect the value of the reward signal time. 

![[Pasted image 20231220172113.png]]

최종적으론  누적 Reward Expectation 값을 최대화 시키는 것을 목표.  J(pi) 이 value function. P(tau|pi) 는 pi 라는 제어기/policy 를 따라서 행동했을 때 어떤 궤적이 나오는지 확인.

![[Pasted image 20231220172517.png]]

초기 state 에서 pi 라는  policy 에 따라서 action 을 했을 때 현재 state 랑 action 에 따라서 그 다음 state 가 어떻게 될 지 확률적인 모델.
![[Pasted image 20231220172914.png]]

These theorem applies same to the Optimal Control Theory. RL is different from Optimal Control that it uses parameterized neural network based controller. Pi_theta which is called Actor tries the maximize the value function by gradient ascent.

![[Pasted image 20231220173211.png]]

The question is how we are going to measure the gradient.

Critic is used to lower the variance. Actor asks the critic about its action to other action

PPO
- Data collection: actor acts and critic evaluates
- Actor update
- critic update
- repeat

## RL in Humanoid
![[Pasted image 20231220173910.png]]

In a humanoid case, it's hard define accurate reward for "good" gait. Thus, regulation lacks due to high DOF results in jerky and "unnatural" behavior/motion.

### Variation 1-1: Regulation through Reference Motion
![[Pasted image 20231220174146.png]]

This method was used in 2018 by DeepMimic which aims to produce target joint angles to mimic mocap data. The reward is motion limitation, but it is trained to maximize the value function (long term reward) over directly matching the mocap data.

State is each link's position/rotation and linear/angular velocity, and Action is qd (30Hz) while using PD controller in 1kHz.

### Variation 1-2: Simplified Model based Reference

![[Pasted image 20231220175105.png]]

SLIP model (inverted pendulum) to give foot pose and velocity reference.
### Variation 2: Task Space Action

![[Pasted image 20231220175325.png]]