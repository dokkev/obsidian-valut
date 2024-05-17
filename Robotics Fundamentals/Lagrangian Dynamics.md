
- Forward Dynamics:
	- Given $\theta, \dot{\theta}$, and, $\tau$, find $\ddot{\theta}$
- Inverse Dynamics
	-  Given $\theta, \dot{\theta}$, and, $\ddot{\theta}$, find  $\tau$

There are two approaches to forward and inverse dynamics problems:
- Lagrangian formulation - variational approach based on kinetic and potential energy of the robot
- Newton-Euler formulation - $F=ma$ applied to each individual link of the robot

### The Lagrangian

$$L(\theta, \dot{\theta}) = K(\theta, \dot{\theta}) - P(\theta)$$
$$
\tau = \frac{d}{dt}\frac{\partial{L}}{\partial{\dot{\theta}}} - \frac{\partial{L}}{\partial{\theta}}
$$
The equation of the motion becomes:
$$ \tau = M(\theta)\ddot{\theta} + c()$$
