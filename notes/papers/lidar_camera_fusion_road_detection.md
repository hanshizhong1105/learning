
### Title
LiDAR-Camera Fusion for Road Detection Using Fully Convolutional Neural Networks

### Main Ideas
* FCN including encoder, context module, decoder without shot bypass connection.
* Cross Fusion: the fusion at different level with weighted summation. The weight parameters are trainable with initialization of zero.
* Compare the early fusion before encoder, late fusion in context module and cross fusion with each layers.
* Evalute on KITTI road benchmark
