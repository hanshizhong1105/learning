There are usurally two methods to use the 3D points clouds for detection:
* Voxelize the irregular point clouds to regular 3D grids and apply 3D CNN detectors
* Project points to regular 2D bird's eye view images and then apply 2D detectors

Proposed **VoteNet** use the recent 3D deep learning models for point clouds directly. 
The backbone of the network is based on **PointNet++**, which has shown sucess in object classificatno and semantic segmentation.
This paper use it for 3D objects detection.\

The entire network can be split into two parts:
* Process existing points to generate votes
  * point cloud feature learning through a backbone network
  * learn hough voting from seed points
* The votes to propose and classify objects
  * Vote clustering through sampling and grouping
  * Proposal and classificatoin from vote clusters
