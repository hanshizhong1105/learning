
### Title
Deep Multi-modal Object Detection and Semantic Segmentation for Autonomous Driving: Datasets, Methods, and Challenges

### Main Ideas
This is a survey paper to summary the datasets, methods, and challenges for the autonomous driving

### Notes

* The methods have very good performance on the KITTI leader-board: HDNET, PointPillars, PixOR, ContFuse, AVOD, F-PointNet, PointRCNN
* Thermal cameras are more robust to daytime/nighttime changes as they detect infrared radiation
* Flash LiDARs can produce detailed object information similar to camera images. 

### Dataset

* Semantic Segmentation datasets include Cityscape, KITTI, Toronto City and ApolloScape. 
* KITTI dataset is recorded in Karlsruhe, which is a mid-sized city in Germany, only during daytime and on sunny days. It labels traking, optical flow, visual odometry, and depth for various computer vision problems. It records 80,256 objects, where ImageNet provides 1M. 
* nuScenes Dataset is the largest dataset with 1.4M frames.

### Great Papers
* 118 Second: sparsely embedded convolutional detecton
* 120 PointNet++
* 126 PointPilloars: Fast Encoders for object detection from point clouds
* 90 AVOD
* 98 Study the pros and cons for for LIDAR representation
* 96 Ensemble Proposals

### Challanges
* Unity Game Engine to produce more simulated datasets
* Increase the efficiency of data labeling
* Sensor Calibration
* Increase the robustness: Dropout, estimate uncertainty, generative models
* The mAP should be evaluate under the different object distance, occlusion, and type of sensors, wheater, daytime.
* Uncertainties to distinguash in- and out-of-distribution
* Incorporate temproal cues
