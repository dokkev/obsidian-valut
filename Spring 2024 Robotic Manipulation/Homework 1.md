An overview of dexterous manipulation, Okamura and Cutkosky, ICRA 2000: 
Section 1, Section 2 until 2.1, Section 3 until 3.1, Section 4 until 4.1, Section 5

Trends and challenges in robot manipulation, Billard and Kragic, Science 2019: you can read all, but more carefully the “Outlook”

–A Review of Robot Learning for Manipulation: Challenges, Representations, and Algorithms, Kroemer, Niekum and Konidaris, JMLR 2021: Section 1, Overview of Learning Problems for Manipulation and Figure 3 (read about the ones you do not know), Section 9

 “challenges, limitations, solved problems and assumptions

, 2) one slide for “Are we progressing in manipulation?” with pro and con arguments,


one slide for “Is learning necessary to solve robot manipulation? How? Why?” also with pro/con arguments.


## An overview of dexterous manipulation, Okamura and Cutkosky, 

#### challenges
- Dexterous Manipulation (DM) requires precise control of forces and motions with robotic hands with fingers.
- Difficulty to locating contact in case of slip with fingertip contact sensors
#### Limitations
- Lack of adequate tactile sensing.

#### Solved Problems
- Kinematic/Dynamic model based manipulation in controlled environments 
- Grasp Jacobian calculates the required fingertip forces from the desired wrench term to the object, while Hand Jacobian maps the relationship between the contact force of the fingertip and joint torques. Moreover, Jacobian can provide kinematic relationship regarding joint velocities, fingertip Cartesian velocity, and object Cartesian velocity.
- 

#### Assumptions
- The rolling and sliding problems are assumed to be pure rolling in the contact plane.
- The sensors at the fingertips can provide reliable and robust measurements (or robust perception system).
- Robustness and smoothness of controllers in switching phases


- Solved problems
- 
- 