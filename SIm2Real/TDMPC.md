### Abstract
- Data driven MPC has advantages:
	- could improve sample efficiency 
	- better performance with increased computational budget
- We combine the strengths of model and model-free
	- learned task-oriented latent dynamics model for local trajectory optimization over short horizon
	- learned terminal value function to estimate long-term return
- As a result, TD-MPC achieves superior sample efficiency and asymptotic performance on both state and image-based continuous control tasks

*Latent Dynamics Model*
- Latent space is a lower dimensional space where the essential features of the original high-dimensional data are preserved.

### Intro
- Model-based learning Is expensive to plan over long horizons
- Model-based methods have historically struggled to outperform simpler model free methods in continuous control tasks.
- MPC optimizes a trajectory over a short, finite horizon due to immense cost of long-horizon planning.
- MPC can be extended to approximate globally optimal soluitions by using a terminal value function that estimates discounted return beyond the planning horizon
- 
