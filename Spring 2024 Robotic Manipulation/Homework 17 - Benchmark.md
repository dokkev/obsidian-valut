## Problem Definition
The need for benchmark arises from the current limitations of robotics and AI in performing long-horizon tasks for human-centered tasks involving complex manipulations tasks. Despite existing benchmarks in simulation, there is a lack of a comprehensive benchmark that addresses the real world diversity of human needs such as activities that humans perform daily, from basic cleaning tasks to more complex interactions with a variety of objects and environment and the physics simulation which can accurately represent physical properties which are necessary for training effective robots.

## Why the state-of-the-art is not enough for this? Why does it fail?
They cannot accurately simulate the physical properties of real-world scenarios, such as the interaction between rigid and deformable objects or the manipulation of liquids, which are crucial for performing everyday tasks. 

## What is the clever idea of this paper?
The benchmark is built upon a survey identifying activities humans wants robots could perform, ensuring relevance and diversity, and it addresses highly realistic physics simulation and rendering which is crucial for vision-based manipulation tasks.

## How the idea is implemented
BEHAVIOR-1K comprises a diverse set of activities, scenes, and objects from physical and semantic properties of 1,000 every day activities defined over 50 different scenes over 5,000 objects.  OMNIGIBSON is built upon Nvidia's Omniverse PhysX to support the simulation of these activities with realistic physics with various materials to enable complex interactions with environments.

##  How is success proved and measured?
Success is measured through experiments that evaluate reinforcement learning algorithms on several activities within BEHAVIOR-1K by evaluating success rates, efficiency, and sim-to-real gap analysis. Success rates are evaluated by task completion rate compared to baseline methods over long-horizon activities. Efficiency is measured by the use of memory and unnecessary movement of objects, and sim-to-real gap is investigated into the discrepancies between simulation results and real-world application. 