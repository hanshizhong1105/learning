### Title
Radar and Camera Early Fusion for Vehicle Detection in Advanced Driver Assitance Systems

### Contribution
* Proposed a deep learning architecture fusing radar and camera ouputs in the early stage

### Techniqual Details
* I think it's a kind of middle stage fusion. Radar branch and camera branch, then feed the concatnated feature into the SSD kinds of networks.

* Both of radar and camera data are transformed to BEV

* The radar data first have some convolution, then send to a polar to cartesion transformation layer and then followed by some comvolutional layers. 

* The camera image first have an invers projection mapping to the BEV and them feeded to several convolutional layers. 

* Result show that SGD is better than ADAM, Freeze the pretrained camera branch can get better performance. 

### Future reading
* 18 Deep Continuous Fusion for Multi-sensor 3D Object Detection
* 32 Pointfusion: Deep Sensor Fusion for 3D Bounding Box Estimation
