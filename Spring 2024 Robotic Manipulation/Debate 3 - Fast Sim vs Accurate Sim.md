- Main benefit of using simulation for robot learning is to
	- improve sample efficiency
	- reduce the cost of data collection
- And having a fast simulation can benefit overall efficiency of data collection or training
- In robot learning, having a larger dataset is more important than having a good quality to avoid covariate shift and achieve task generalization. 
- To overcome lack of accuracy in simulation, numerous sim2real transfer techniques such as domain randomization and domain adaptation, meta-learning, and knowledge distillation have been introduced.  

- Speed of the simulation is crucial in RL
- The nature of RL involves learning by interacting with environments requiring numerous trials (samples) to learn policies. Faster simulation allows more interactions in a shorter period of time enhancing the learning process.
- RL involves a lot of experimentation with different algorithms, parameters, and models. Fast simulations make it feasible to test more configurations and thus find optimal solutions faster.
- For applications requiring real-time decision-making,  fast simulations enable algorithms to learn and adapt in environments close to real-time
- As the complexity of tasks and environments increases, the need for more computational power and faster simulations becomes critical. Fast simulations ensure that as models and environments grow more complex



#### Transfer Learning
It aims at improving the performance of target learners on target domains by transferring the knowledge contained in difference but related source domains

#### Domain Adaptation
Subset of transfer learning. It specifies the situation when we have sufficient source domain labeled data and the same single task as the target task, but without or very few target domain data

#### Policy Distillation
 the process of extracting knowledge to train a new network that is able to maintain a similarly expert level while being significantly smaller and more efficient

#### Meta Learning
Meta Learning, namely learning to learn, aims to learn the adaptation ability to unseen test tasks from multiple training tasks.