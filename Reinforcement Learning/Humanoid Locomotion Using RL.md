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
### Variation 2-1: Task Space Action

![[Pasted image 20231220175325.png]]
![[Pasted image 20231220175917.png]]
Policy, pi outputs task space action xd which is fed into the OSC. OSC needs to ran along with the learning. 

RL is beneficial in robustness that action is affected by noise which results in both bad and good action which results in compliant controller in case of disturbance
### Variation 2-2

- Vision included hierarchical structure
- RL based low level controller
### Sim-to-Real Issue
Due to simulation and reality gap, learned controlled may not perform well in the real robot. To mitigate these issues:
- Accurate system identification (link, mass, actuator performance)
- Dynamics/Domain randomization but this method decreases optimal performance
- Sensor noise
- Curriculum learning: start with easier task such as lower speed
- Domain Adaptation  (Online system identification): Estimate randomized parameters in real robot deployment.

### Real Robot Experiment
- Task 1: stand-still task with torque command
	- State: Jpos/vel, Body orientation
	- Command torque of 33 joints
	- Reward: Body pose6d, Joint pose6d
- Task 2: Squat
	- State
		- Orientation (roll, pitch)
		- Joint Positon
		- Joint Velocity
		- Phase : 전체 모션중 현재의 시간을 표현
	- Action
		- Torque of 33 joints
	- Reward
		- Body Orientation Stability
		- Joint Position mimic
		- Joint Velocity mimic
	- Since the policy affects the whole body, the upper body error affects lower body and vice-versa.
- End-to-end method is more sensitive to the model difference.
- Position control with PD controller compensate for error such as friction resulting similar state transition between the simulation and the real robot.
- On the other hand, torque output creates a large gap in state transition.