### Abstract
- Data driven MPC has advantages:
	- could improve sample efficiency 
	- better performance with increased computational budget
- We combine the strengths of model and model-free
	- learned task-oriented latent dynamics model for local trajectory optimization over short horizon
	- learned terminal value function to estimate long-term return
- As a result, TD-MPC achieves superior sample efficiency and asymptotic performance on both state and image-based continuous control tasks

*Latent Dynamics Model*
- Latent space is
