
When we talk about general-purpose robots. It usually requires two features:
one is generalization and the other one is safety. I argue that solely scaling imitation learning does not guarantee the robot policy is able to generalize task and adapt to dynamic environment safely.


The first reason is adaptability requires a high quality set of demonstration for training in imitation learning.
- Teleoperation of the real robot is one of the most effective methods to obtain data from demonstration.
- But most available teleoperation devices lack of kinesthetic feedback, while force and torque are significant information in contact-rich manipulation task.
- Recent robot data collection hardware such as mobile ALOHA and Universal Manipulation Interface from Stanford showed impressive results of policy learning platform with simple teleop interfaces, their examples were limited to manipulating light and small objects. 
- Scaling imitation learning for better adaptability against perturbation makes the training very expensive because it requires good kinesthetic perception and actuation on both robot and teleoperation devices. 
- And that becomes a limiting factor for scaling imitation learning for general purpose robotics. 


Lastly, the second reason is  lack of safety measure on
- task generalization is a big challenge in robotic manipulation, and
- There have been many attempts at generalization method 
- such as Inverse RL, Meta Learning, Multi-Task Learning, Transfer Learning, Multi-Task RL, Lifelong Learning, and continual learning. 
- However, those approaches have no emphasis on control-theoretical guarantees such as stability and boundedess which are critical to safety.
- Without  assurance of safety, policy can not be deployed for general-purpose robotics


## Terminology
#### Control-theoretical guarantees 
assurances provided within the framework of control theory, which ensure that a control system behaves as expected under certain conditions.
- Stability
- Convergence
- Robustness
- Optimality
- Boundedness
-  Reachability and Controllability

### Generative adver-sarial learning framework
- randomly explores for corrections that bring the policy close to the demonstrated distribution.
- require either constant human effort or lots of data and computation and hold no control-theoretic guarantees on the learned policy
- trade-off is the training process involves frequent interaction with the environment and could be more fragile and not stable for saddle point problem



## pro

q: is sufficientt enough?

reward - query -env - reward

why?
scaling works well in LLM
massive data
tokens 

why not robotics?
sturcture in lang  well tuned in transformer
not same match for robotics
traj differnt from language
not enough data not engouth model
RM3 papaer took transformer for robotics using vid
imitation learning - 
gnerealize high level-  vision and language
lowe level - robustnss fine turn



