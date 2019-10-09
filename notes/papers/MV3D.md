### Title
Multi-View 3D Object Detection Network for Autonomous Driving

### General Idea
* **2-stage method with bbox proposal network and second stage refinement**
* A sensory-fusion framework that takes both LiDAR point cloud and RGB images as input and predict oriented 3D bounding boxes. 
* The framework include two subnetworks: one for 3D object proposal generation and another for multi-view feature fusion. 
* The proposal network generates 3D candidate boxes from the BEV representation of 3D point cloud. 
* The deep fusion scheme is proposed to combine region-wise featrues from multiple views and enable interactions between intermediate layers of different paths. 

### Contributions:
* Deep Fusion
* Multi-View 3D Fusion of BV/FV/RGB branch.

### Techniqual Details
* BEV representation: Height, Intensity and Density. Height is computed as the maximum height of the points in each cell and each slices. The intensity is the maximum height in each cell along all slices. The density indicates the number of points in each cell along all slices. 
* The Front View Representation is a cylinder plane c and r. The front is defined as reference with the ego-car. 
* The 3D proposals are generated based on BEV input with 3 reasons. 1) preserve the physical sizes. 2) avoiding occlusion. 3) obtain accurate 3D bounding boxes. 
* Deep fusion is element-wise mean with drop-out operation of different views for regularization.
* Oriented 3D Box Regression: 8 corners points with 24-D vector regression works better than the centers and sizes with 6-D vector regression. 

### Key Notes
* In overall, image-based methods usually perform better than LiDAR-based methods in terms of 2D detection. 


