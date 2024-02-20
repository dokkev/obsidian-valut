
When we talk about general-purpose robots. It usually requires three features:
First one is generalization,  the second one is adaptability, and the thrid one is safety. I argue that solely scaling imitation learning does not guarantee the robot policy is able to generalize task and adapt to dynamic environment safely.

The first reason is generalization is 

The second reason is adaptability requires a high quality set of demonstration for training
- Teleoperation of the real robot is one of the methods to obtain data from demonstration. For imitation learning
- But most available teleoperation devices lack of kinesthetic or tactile feedback while force


Lastly, the third reason is  safety
- Task generalization is a big challenge in robotic manipulation, and
- There have been many attempts at generalization method 
- such as Inverse RL, Meta Learning, Multi-Task Learning, Transfer Learning, Multi-Task RL, Lifelong Learning, and continual learning. 
- However, those approaches have no emphasis on control-theoretical guarantees such as stability and boundedess which are critical to safety


- Dilemma of transferability
	- Kinesthetic teaching enables proprioceptive perception from the expert's demonstration, but the effectiveness of this method is limited to the physical capabilities of the robot in terms of force, torque, and tactile sensing. 


## Terminology
#### Control-theoretical guarantees 
assurances provided within the framework of control theory, which ensure that a control system behaves as expected under certain conditions.
- Stability
- Convergence
- Robustness
- Optimality
- Boundedness
-  Reachability and Controllability

### Generative adversarial (에드벌세뤼얼) learning framework
- randomly explores for corrections that bring the policy close to the demonstrated distribution.
- require either constant human effort or lots of data and computation and hold no control-theoretic guarantees on the learned policy
- trade-off is the training process involves frequent interaction with the environment and could be more fragile and not stable for saddle point problem