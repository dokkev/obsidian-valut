- **Problem definition** 1-2 sentences
- **Why the state-of-the-art is not enough for this? Why does it fail?** 1-2 sentences
- **What is the clever idea of this paper?** 1-2 sentences
- **How the idea is implemented? (algorithm, network structure, system...)** 2-3 sentences
- **How is success proved and measured? (experiments, metrics, most relevant result)** 1-2 sentences

### Problem Definition
Autonomously grasping a previously unknown object is challenging due to difficulty of accurate full 3D reconstruction of first-seen object through vision since sensors such as camera and laser sensors can only reconstruct visible portion or the front face of the object. 

### Why the state-of-the-art is not enough for this? Why does it fail?
Triangulation of 3d grasping points heavily depend on stereo vision, and the quality of stereo vision affects the accuracy of grasping points. 

### What is the clever idea of this paper?
It attempts to extract visual features for grasping points, and it is a cost-effective method because it eliminates the necessity to project every pixel of the image. 

### How the idea is implemented
The algorithms takes two or more images of an object from different locations, then grasping points are identifiesd 