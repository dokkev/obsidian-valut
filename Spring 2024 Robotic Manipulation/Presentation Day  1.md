### Jonathan: Collaboration
- Trajectory adaption though CV and Speech command
- sensed force (torque sensing at joint?)
- Learned classifier
	- different action -> depends on state transition
- Fast LfD, updating and adapting learned models

### Heath: Hierarchical RL
- high-D action spaces and state spaces
- reducing the action spaces to finite may improve
- Instantaneous Screw Axis TF and Clustering as previous work
- Goals
	- utilize movement primitives to train a policy (execute predicted trajectories)
- BC with LSTM : input-> encoder decoder ->dense -> output
- EE position? -> is it doing IK?

### Fernando: Learning to compensate for friction
- good for compliant controller
- dependent on temp, angle, velocity,....
- It's hardware specific
- OSC
- u_f = u - f_theta
- desired ee -> osc -> tau -> sim1 (control + friction torque) -> known torque frictional torque
- Assuming that simulation has good friction model
### Abayomi and Evan: Goal conditioned RL
- RL not scalable
- GCRL for grasping
- GCRL: RL where the reward signal is also dependent on some goal states

### Sharan and Shah: Fine-tuning VLM for Robotic Planning Task
- Inte