
- Forward Dynamics:
	- Given $\theta, \dot{\theta}$, and, $\tau$, find $\ddot{\theta}$
- Inverse Dynamics
	-  Given $\theta, \dot{\theta}$, and, $\ddot{\theta}$, find  $\tau$

There are two approaches to forward and inverse dynamics problems:
- Lagrangian formulation - variational approach based on kinetic and potential energy of the robot
- Newton-Euler formulation - relies on $F=ma$ applied to each individual link of the robot

## The Lagrangian

$$L(\theta, \dot{\theta}) = K(\theta, \dot{\theta}) - P(\theta)$$
$$
\tau = \frac{d}{dt}\frac{\partial{L}}{\partial{\dot{\theta}}} - \frac{\partial{L}}{\partial{\theta}}
$$
The equation of the motion becomes:
$$ \tau = [M(\theta)\ddot{\theta} + c(\theta, \dot{\theta}) + g(\theta)] + J^T(\theta)F_{tip}$$
$$  = [M(\theta)\ddot{\theta} + C(\theta, \dot{\theta})\dot{\theta} + g(\theta)] + J^T(\theta)F_{tip}$$
$$  = [M(\theta)\ddot{\theta} + h(\theta,\dot{\theta})] + J^T(\theta)F_{tip}$$
- $c$ : velocity product term
- $C$ : Coriolis matrix

The velocity product term can be re-written as:
$$ \tau = M(\theta)\ddot{\theta} + \dot{\theta}^T\Gamma(\theta)\dot{\theta} + g(\theta) $$


![[Pasted image 20240517003630.png]]
![[Pasted image 20240517003535.png]]
![[Pasted image 20240517003649.png]]
