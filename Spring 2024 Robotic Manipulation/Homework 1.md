

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


An overview of dexterous manipulation, Okamura and Cutkosky, ICRA 2000: 
Section 1, Section 2 until 2.1, Section 3 until 3.1, Section 4 until 4.1, Section 5

Trends and challenges in robot manipulation, Billard and Kragic, Science 2019: you can read all, but more carefully the “Outlook”

–A Review of Robot Learning for Manipulation: Challenges, Representations, and Algorithms, Kroemer, Niekum and Konidaris, JMLR 2021: Section 1, Overview of Learning Problems for Manipulation and Figure 3 (read about the ones you do not know), Section 9

 “challenges, limitations, solved problems and assumptions

, 2) one slide for “Are we progressing in manipulation?” with pro and con arguments,


one slide for “Is learning necessary to solve robot manipulation? How? Why?” also with pro/con arguments.
