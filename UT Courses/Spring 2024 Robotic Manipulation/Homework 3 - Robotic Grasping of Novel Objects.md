
### Problem Definition
Autonomously grasping a previously unknown object is challenging due to difficulty of accurate full 3D reconstruction of first-seen object through vision since sensors such as camera and laser sensors can only reconstruct visible portion or the front face of the object. 

### Why the state-of-the-art is not enough for this? Why does it fail?
Triangulation of 3d grasping points heavily depend on stereo vision, and the quality of stereo vision affects the accuracy of grasping points. This method is limited to static object, and the scalability of the algorithm requires sufficient training of diverse objects to handle non-uniform density objects.
### What is the clever idea of this paper?
It attempts to extract visual features for grasping points, and it is a cost-effective method because it eliminates the necessity to project every pixel of the image.  Using synthetic images allow robust perception by varying light conditions, object features, and extrinsic parameters of the camera.

### How the idea is implemented
The algorithm is trained using supervised learning with grasping points labeled computer generated images with variation of object conditions. The algorithms take two or more images of an object from different locations, then possible grasping points are identified using their probabilistic model to overcome uncertainty (error) due to the location of the camera. It models errors using Additive Gaussian in 2D image, uses logistic regression to estimate the grasping points, and determine the 3D grasping points using MAP inference.

###  How is success proved and measured?

The predictive accuracy of the algorithm is tested by feeding images not contained in the training dataset. Then the experiment conducts grasping objects similar to training images and novel objects using a real mobile robotic platform and the author's algorithm and measures grasp success rate and mean error of locating grasp points  