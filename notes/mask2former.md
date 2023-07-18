## This paper can do all the segmentation at the same time. 
The previous paper MaskFormer has a backbone, a pixel decoder, and a Transformer decoder. The pixel decoder and transformer decoder a deeply connected with cross-attention. In this paper, we use masked attention.
### What's the masked attention? what's the motivation for masked attention? What's the benefit?
* Transformer-based global cross-attention can slow the convergence. The local features-based transformer is good enough for updating query features.
* For the cross-attention, the query is learned. The value and key are the image features under transformation.
* For the masked-attention, the result of the query multiple key will add the Mask before the softmax. The mask is a binary mask. 
* 

