
### Title
HDNET: Exploiting HD Maps for 3D Object Detection

### Contribution
* Use the Hight-Definition (HD) maps to boost the performance and robustness of 3D object detection. 
* Extracts geometric and semantic features from the HD maps
* If the HD maps are not available, the predicted mapo can be estimated on the fly from the raw LiDAR data
* Conduct the experiments on KITTI and TOR4D datasets. 

### Techniqule Details
* The input are the maps generated from the LiDAR points cloud
* Treat the Z axis as feaeture channel and exploit 2D convolutions. 

### Key Notes
* The HD maps contain geometric and semantic information about the enviroment
* The geometric information is the point-wise geometric
* The sementci information includes ground and road pixel-wise binary value
