Operational Space 는 로봇이 실제 작업을 수행하는 공간을 의미
가끔식 Task Space 라고 불리기도 함.
-> End-effector 가 Task Space 에서 원하는 pose 에 도달하거나 특정 Force 를 출력하고자 할 때, 필요한 Torque 는 얼마인가?

Object in Task Space is described using SE(3) and SO(3). 

### Work and Power

$$
W = \int{F^{T}v *dt} = F^{T} d
$$
$$ P = \frac{W}{t} = \frac{F^Td}{t}= F^{T}v$$
$$ W$$