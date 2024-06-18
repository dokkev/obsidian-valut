### Introduction
- While past robotics have focused on rapid and accurate pick-and-place position control in controlled environments, future mobile robots must be capable to manager broader dynamic and force-critical interactions in unstructured environments. 
- Legged locomotion involves repeating dynamic events such as impact, high-force interactions with uncertain terrain, and rapid leg swing. 
- Such things make designing EM actuators challenging. 
- Design processes of EM were traditionally governed by performance metrics such as the motor constant, torque constant, peak torque, continuous torque, thermal capacity, etc.
- Speed reducer is a critical component that affects the control bandwidth and ability to handle collisions with the environment. 
- Therefore, proprioceptive actuator is proposed that allows  "proprioceptive" foot force control through internal torque control without exteroceptive sensory feedback that is known to cause non-collocated sensing problems upon collision which result in contact instability.

#### Torque Density
- Achieving high torque with a minimum actuator mass is critical due to high ground reaction force (GRF) required to propel
- Simply employing large motors is not viable since it contribute to GRF requirement
- This highlights the importance of maximizing torque density.

#### Energy Efficiency
- Locomotion is a typically energy dissipative process and the loss mechanisms are categorized into three major modes:
	- Joule heating
	- Transmission
	- Interaction losses
- Low gear ratios will reduced the reflected inertia but can cost higher energy in generating torque via Joule heating. 
- High gear ratios may improve energetics in theory but can break a leg upon contact or even could prevent a desired dynamic motion due to excessive mechanical impedance. 
- 