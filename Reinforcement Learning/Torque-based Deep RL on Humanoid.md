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

PD 제어의 문제점
- PD predetermines the behavior
- Each task needs own tuning 
- lack of compliance
- Due to reality gap, there is a joint tracking performance difference and contact timing mismatch (학습된 contact timing 과 다름)
- When an unexpected contact occurs, the PD controller tries to reduce the tracking error

Torque 기반의 제어를 통해 PD 튜닝을 없게
토크 제어의 고유한 compliance 덕에 reality gap 에 강인함

토크제어가 학습이 느리니 -> Gravity Pre-training

위치제어 RL :
- Output 이 q_target 이라 직관적
- 학습이 빠름 -> 학습 시작부터 pose 를 유지가능
- Compliance 가 부족함
Therefore, Graviry pre-training
- collect pre-training data (gravity torque) at random poses
- Pre-train the policty