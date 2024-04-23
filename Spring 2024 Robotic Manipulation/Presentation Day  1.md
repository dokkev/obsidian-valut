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
- 