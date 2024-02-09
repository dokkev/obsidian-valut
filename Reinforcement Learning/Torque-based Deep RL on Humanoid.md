Different task requires different control strategies. From biological view, human can control joint compliance which determined by the number of parallel elastic elements in muscle activation. 

![[Pasted image 20240208222550.png]]


The robot's compliance is determined by the PD gain in the controller.
![[Pasted image 20240208222837.png]]

강화학습에서 기초적으로 두가지 구조:
- 위치기반 구조
	- q_target -> PD controller
-  토크제어
	- tau_cmd
- 대부분의 연구들은 위치기반 RL

"Learning Locomotion Skills Using DeepRL: Does the Choice of Action Space Matter?" (2017)
- compared action spaces with respect to learning speed, motion quality and limitation in simulation only
	- torque control
	- Joint control with PD
	- joint velocity
	- muscle activation (?)
- Results: Torque learning is slow and not robust to perturbation (at low control rate)
