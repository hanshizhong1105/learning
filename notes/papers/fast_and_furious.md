### Title
Fast and Furious: Real Time End-to-End 3D Detection, Tracking and Motion Forecasting with a Single Convolutional Net

### General Idea
3D convolutions acrross space and time over a bird's eye view (BEV) representation of the 3D world, which is very effcient in term of both memory and computation. 

### Contribution

* The proposed method can **join 3D detection, trakcing and motion forecastsing**. 
* Fast as real-time 30ms. 
* Evaluated in a very big Uber inhouse dataset. 

### Techniqual Details
* Input **only the LiDAR data** is 4D tensor (time, height, X, Y). The 3D world is quantized to form a 3D voxel grid. Each voxel encoding whether the voxel is occupied if there exists at least one point in the voxel's 3D space. 
* For the input 3D voxel data, we first perform a 2D convolutions and treat the height dimension as the channel dimension.
* Exploit 3D convolutions over space and time.
* Early Fusion: first use a 1D convolution with kernel size n on temporal dimension to reduce to 1, and them perform 2D convolutions by treating the height dimension as the channel dimension.
* Late Fusion: For each timestamp, the 2D convolution is performed as the early fusion. Then perform 3D convolution with kernel size 3*3*3 for 2 layers without pading on temporal dimension, which can reduce the temporal dimension from n to 1. Final, the 2D spatial convolutions were performed. 
* The loss is same as the SSD including classificaiton loss and regression loss of bbox over **the current and n-1 future frames**. The regression target including lx, ly, sw, sh, asin, and acos. 
* The experiments were performed in Uber's inhouse dataset which is 2 orders of magnitude bigger than KITTI. 


### Key Notes
* Self-driving has four steps:
  1. Detection
  2. Object tracking
  3. Motion forecasting
  4. Motion planning
  

