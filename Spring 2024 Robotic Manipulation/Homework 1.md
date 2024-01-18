

## An overview of dexterous manipulation, Okamura and Cutkosky, 

#### challenges
- Dexterous Manipulation (DM) requires precise control of forces and motions with robotic hands with fingers.
- Difficulty to locating contact in case of slip with fingertip contact sensors

1. **Tactile Sensing**: A major limitation is the lack of adequate tactile sensing for robust manipulation control. This limits autonomous robotic dexterous manipulation to research laboratories (Page 1).
2. **Kinematic Relationships**: The kinematic and force relationships in dexterous manipulation are complex, often leading to over-constrained or under-constrained systems (Page 3).
3. **Contact and Rolling Constraints**: Incorporating rolling and sliding constraints in kinematics involves complex differential geometry, requiring precise control of contact point velocities (Page 3).
4. **Contact Types and Force Closure**: Grasping stability and manipulation are strongly influenced by contact conditions at the fingertips, including frictional constraints and soft finger contacts (Page 4).
5. **Grasp Planning and Optimizations**: Grasp choice and motion planning algorithms are currently slow and require offline computations, making real-time autonomous manipulation challenging (Page 5).
6. **Hardware Limitations**: Actuators are often not sufficiently small, lightweight, or backdrivable for dexterous manipulation. Sensor technology, crucial for feedback, is still inadequate in many aspects (Page 7).
7. **Software Complexity**: The mathematical complexity, particularly in 3D rolling and sliding manipulations, poses significant challenges in developing effective control algorithms (Page 8).
#### Limitations
- Lack of adequate tactile sensing.

#### Solved Problems
- Kinematic/Dynamic model based manipulation in controlled environments 
- Grasp Jacobian calculates the required fingertip forces from the desired wrench term to the object, while Hand Jacobian maps the relationship between the contact force of the fingertip and joint torques. Moreover, Jacobian can provide kinematic relationship regarding joint velocities, fingertip Cartesian velocity, and object Cartesian velocity.
- Planning can involve understanding of the reachability, workspace governed by kinematics and contacts, and regrasping to generate serial motions to manipulate an object.

#### Assumptions
- The rolling and sliding problems are assumed to be pure rolling in the contact plane.
- The sensors at the fingertips can provide reliable and robust measurements (or robust perception system).
- Robustness and smoothness of controllers in switching phases
- Accurate perception of object state (such as 6D pose)

1. **Model-Based Approach**: The model-based approach to manipulation, based on kinematics and dynamics of manipulating objects with fingertips, has seen adequate development for controlled environments (Page 1).
2. **Kinematic Measures**: Development of kinematic measures useful in dexterous manipulation, like grasp Jacobian and hand Jacobian, which help in calculating required contact forces and joint torques (Page 2).
3. **Contact Point Analysis**: Analysis of rolling and sliding at contact points, and the development of constraints for pure rolling in the contact plane (Page 3).

### Future Directions:

- The paper suggests that future applications may include underwater salvage, remote planetary exploration, and retrieval of objects from hazardous environments (Page 1).
- A shift towards supervised manipulation, where humans provide high-level planning, and robots perform fine manipulations, is seen as a promising direction (Page 8).


## Trends and challenges in robot manipulation, Billard and Kragic, Science 2019


1. **Ongoing Challenge in Dexterous Manipulation**: Despite advancements in software and hardware, achieving dexterous manipulation in robots - the ability to handle objects with precision and variety similar to human hands - remains an unsolved and complex issue. This challenge is intriguing as it requires a deeper understanding of human grasping and manipulation techniques.
    
2. **Purpose of Building Robots**: Robots are developed not only to automate tasks but also to assist humans in performing repetitive or dangerous tasks safely. This reflects the dual role of robots in both replacing and augmenting human efforts.
    
3. **Robust and Flexible Human-Robot Collaboration**: The future of robotics aims at seamless collaboration between humans and robots. This involves removing physical barriers ("fences") that currently exist for safety reasons and enabling direct interaction.
    
4. **Integration into Human Environments**: For robots to work alongside humans effectively, they need to be able to interpret human intentions and respond appropriately. This requires robots to be "smooth and trustable partners," suggesting they should operate in a way that is predictable, reliable, and easy for humans to understand and interact with.
    
5. **Understanding Human Interaction**: Robots need to have a better grasp of human behavior and interaction dynamics. This involves understanding both verbal and non-verbal cues and adapting to them in real-time.
    
6. **Real-time Adaptation**: Robots should be capable of adapting their actions in real-time based on changes in their environment or in response to human actions. This adaptability is crucial for effective and safe collaboration.
    
7. **Safety by Design**: There is a need to develop robots with safety as a fundamental aspect of their design. This includes creating robots with soft and lightweight structures to minimize the risk of injury during interactions.
    
8. **Multisensory Feedback-Based Control and Planning**: The paragraph also emphasizes the importance of advanced control and planning methodologies for robots, which should incorporate multisensory feedback. This means using data from various sensors (touch, vision, etc.) to make more informed and nuanced decisions.

### Page 1: Introduction

- **Background**: Initially, robotic manipulation consisted of pre-defined movement sequences without environmental adaptation. Over time, advances in AI and control theory have improved robots' ability to handle errors, uncertainties, and adapt forces upon contact.
- **Current Challenges**: Achieving dexterous manipulation, robust perception, and adaptive control in dynamic environments remain significant challenges.
- **Future Outlook**: The paper envisions robots working alongside humans, necessitating improved human-robot collaboration, safety by design, and multisensory feedback-based control and planning methodologies.

### Page 2: Current Capabilities and Limitations

- **Capabilities**: Robots excel in repetitive and structured settings like industrial assembly, where object properties are known.
- **Limitations**: Handling of deformable objects and performing tasks requiring fine manipulation, such as handwashing dishes or peeling potatoes, remain beyond current robotic capabilities.
- **Hardware and Software Development**: Advanced software and hardware are required for better sensory integration and cognitive capabilities in robots.

### Page 3: Designing Robotic Hands

- **Soft Hands**: Recent designs aim to mimic human hand's natural compliance using soft actuators and materials.
- **Sense of Touch**: Development of touch sensors for robots is crucial for precise manipulation, with a focus on integrating stretchable artificial skin for comprehensive contact measurements.

### Page 4: Perception and Control

- **Multimodal Perception**: Successful manipulation involves integrating visual, haptic, and other sensory modalities.
- **Challenges in Perception**: Recognizing partially occluded objects and integrating visual and haptic information remain areas for improvement.

### Page 5: From Grasping to Manipulation

- **Grasping Theory**: The paper discusses the theoretical aspects of forming a stable grasp, including the challenges in incorporating uncertainties from object models and interaction dynamics.
- **Data-Driven Approaches**: Recent trends include using databases of grasps for known and unknown objects, with a focus on adapting to different object properties.

### Page 6: Advanced Manipulation Challenges

- **In-Hand Manipulation**: Discusses the complexity of actions like twirling a pen or preparing a key for insertion, emphasizing the need for both intrinsic and extrinsic dexterity.
- **Bimanual Manipulation**: Highlights the underdeveloped area of dual-arm manipulation and the integration of object representation and movement primitives.

### Page 7: Learning for Manipulation

- **Continuous Learning**: Emphasizes the need for robots to continuously learn and adapt their perception and control for unfamiliar objects.
- **Limitations of Learning**: Addresses the challenges in relying solely on learning methodologies, including the need for substantial training data and the difficulty of modeling complex non-rigid objects.


## A Review of Robot Learning for Manipulation: Challenges, Representations, and Algorithms, Kroemer, Niekum and Konidaris, JMLR 2021:

#### Section 4: Learning Object and Environment Representations
The robot must discover the state features and degrees of freedom attached to each object in its environment.

##### 4.1 Object Representations

- **Modular Representation**: The world is divided into objects, each described by features or properties. This includes movable objects like mugs, tables, doors, and stationary objects like counters and walls. Robots create a modular representation by segmenting the environment into objects and estimating their properties.
- **State and Context Spaces**: Object representations capture variations within tasks (state space) and across tasks (context space). For example, in a block stacking task, the shapes and sizes of the blocks (context) are fixed for a given task but vary across different tasks.
- **Hierarchical Representations**: Object models are represented hierarchically, with layers corresponding to point-, part-, and object-level representations, each decreasing in detail but increasing in abstraction. This structure mirrors the geometric structure of objects and their parts.

##### 4.2 Discovering Objects and Their Properties

- **Segmentation and Identification**: Robots distinguish individual objects in a scene, typically using passive perception. They maintain a probabilistic belief over whether different parts belong to the same object and use interactive perception or viewpoint selection to resolve ambiguities.
- **Learning Object Properties**: Robots learn about objects and their properties from data. This includes learning about variations in objects' features and how these variations are relevant to different manipulation tasks.

##### 4.3 Learning About Objects and Their Properties

- **Discovering Objects**: The first step in learning is distinguishing individual objects in a scene, which is a segmentation problem, typically accomplished using passive perception. However, objects may often be close together in the scene, presenting the robot with ambiguous information about object identity.
- **Interactive Perception**: The robot can maintain a probabilistic belief over whether or not different parts belong to the same object, and use interactive perception or viewpoint selection to clarify the identity of objects.

#### Section 5: learning a transition model of the environment (Sec. 5)
The robot must learn a model of how its actions aﬀect the task state, and the resulting background cost, for use in planning.

##### 5.1 Continuous Models

- **Concept**: Discusses continuous models where the transition function is represented as a continuous function, often a neural network.
- **Challenges**: The challenges in using continuous models include handling the high dimensionality of the input space and the need for large amounts of training data.

##### 5.2 Discrete Models

- **Overview**: This subsection talks about discrete models, which are particularly useful in symbolic or highly structured environments.
- **Approach**: These models often employ propositional logic to define states and transitions, allowing for compact and understandable representations of the environment.

##### 5.3 Hybrid Models

- **Combination of Continuous and Discrete**: Hybrid models combine elements of both continuous and discrete models. They are often used in scenarios where manipulation tasks have both discrete and continuous aspects.
- **Application**: These models are crucial in handling tasks that involve both high-level decision-making and fine-grained control.

##### 5.4 Learning Transition Models

- **Learning Process**: This part discusses the process of learning transition models from data. It covers the different strategies robots can use to understand how their actions change the environment.
- **Data Collection**: Emphasizes the importance of data collection strategies in learning accurate and generalizable models.

Overall, Section 5 provides a comprehensive overview of how robots can model and learn the dynamics of their actions in the environment, using continuous, discrete, and hybrid models. It highlights the importance of these models in enabling robots to plan and execute tasks effectively in a variety of settings.

#### Section 6: Learning motor skills
the robot attempts to learn a motor control policy that directly achieves some goal, typically via reinforcement learning

#### Section 7: 

Section 1, Overview of Learning Problems for Manipulation and Figure 3 (read about the ones you do not know), Section 9

 “challenges, limitations, solved problems and assumptions

, 2) one slide for “Are we progressing in manipulation?” with pro and con arguments,


one slide for “Is learning necessary to solve robot manipulation? How? Why?” also with pro/con arguments.
