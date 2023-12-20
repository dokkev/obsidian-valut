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


![[rl_framework.png|500]]


RL environment involves an Agent and Environment. The Agent takes action based on the State, and the Environment provides next State and Reward to the Agent.

![[reward_eq.png]]

The goal is to maximize the accumulative reward over instantaneous reward. Gamma is a discount factor which reflect the value of the reward signal time. 

![[Pasted image 20231220172113.png]]

최종적으론  누적 Reward Expectation 값을 최대화 시키는 것을 목표.  J(pi) 이 value function. P(tau|pi) 는 pi 라는 제어기/policy 를 따라서 행동했을 때 어떤 궤적이 나오는지 확인.