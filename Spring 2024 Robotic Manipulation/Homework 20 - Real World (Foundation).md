## Lessons from the Amazon Picking Challenge: Four Aspects of Building Robotic Systems

## Problem Definition
The Amazon Picking Challenge tested the ability of a robotic system to autonomously pick the ordered items from a warehouse shelf. This paper describes the winning entry to this competition and how they approached manipulation problems in real world unstructured environments.
## Summary of the methodology presented: algorithm, input-output
The methodology is characterized by its approach to system building along four key aspects, each offering a spectrum of solutions.
Modularity vs. Integration: Emphasizes the importance of system integration over individual module performance, advocating for a balance between modularity for problem simplification and integration for effective system behavior.
Computation vs. Embodiment: it suggests that robot behavior emerges from both computation and embodiment , recommending a blend where hardware adjustments can lead to simple, robust solutions.
Planning vs. Feedback: it highlights the trade-off between planning (searching in a world model for verifiable solutions) and feedback (reducing uncertainty through physical interaction), with a preference for feedback when global search is not necessary.
Generality vs. Assumptions: Discusses the need for general solutions while acknowledging the importance of making reasonable assumptions to tackle manipulation challenges in unstructured environments effectively.

## Applicability / Problems solved
It addresses the problem of autonomously picking and placing diverse objects from a cluttered warehouse shelf, under varying and challenging conditions such as lighting and object placement. This method can be applied to light objects warehouse automation without cumbersome parameters tuning. 
## Assumptions and limitations
This method assumes the value of tightly integrated systems and the importance of embodying computation into hardware where feasible. Limitations involves dealing with unexpected object orientations and the need for further exploration in planning for in-bin object reorientation. 