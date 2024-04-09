## Lessons from the Amazon Picking Challenge: Four Aspects of Building Robotic Systems

## Problem Definition
The Amazon Picking Challenge tested the ability of a robotic system to autonomously pick the ordered items from a warehouse shelf. This paper describes the winning entry to this competition and how they approached manipulation problems in real world unstructured environments.
## Summary of the methodology presented: algorithm, input-output
The methodology is characterized by its approach to system building along four key aspects, each offering a spectrum of solutions:
- Modularity vs. Integration: 
- Computation vs. Embodiment: 
- Planning vs. Feedback: 
- Generality vs. Assumptions: 
Using a holonomic mobile 7-dof manipulator with suction-cup gripper, FT sensor, RGBD camera, laser range finder, two motion generations which are top-down and side picking are used depends on likelihood of success. The robot's motion is govened by sensor 
## Applicability / Problems solved
It addresses the problem of autonomously picking and placing diverse objects from a cluttered warehouse shelf, under varying and challenging conditions such as lighting and object placement. This method can be applied to light objects warehouse automation without cumbersome parameters tuning. 
## Assumptions and limitations
This method assumes the value of tightly integrated systems and the importance of embodying computation into hardware where feasible. Limitations involves dealing with unexpected object orientations and the need for further exploration in planning for in-bin object reorientation. 