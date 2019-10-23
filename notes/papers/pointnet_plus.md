### Title
PointNet++ and PontNet

### Main Contribution
* Proposed a hierarchical neural network that applies PointNet Recursively on a nested parititioning of the input point set. 
* By exploiting metric space distance, our netowrk is able to learn local features with increasing contextual scales. 
* With dropout, the proposed novel set learning layers can adaptively combine feature from mutiple layers

### Notes

* PointNet is an effective architecture to process an unordered set of points for semantic feature extraction. 
* The set sbstraction level is make of three key layers: sampling layer, grouping layer and pointnet layer. 
* The pointnet predict an affine transformation matrix by a mini-network (T-net) and directly apply this transformation to the coordinates of input points
* THe transformation matrix is reglarized by a orthogonal regularization term.


