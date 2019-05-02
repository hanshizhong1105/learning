
# Introduction:
* A training interface based on Tensforflow
* High-level APIs for training
* Tensorpack brings speed and flexibility together vs Keras
* Tensorflow itself is fast, but it should be written in an efficient way
* It includes the following library: DataFlow, InputSource, ModelDesc, Trainers, Callbacks and so on

# DataFlow
* Build Python iterators for efficient data loading
* Independent of Tensorflow
* A common pipeline includes:
  * Read from disk or other source
  * Apply transforms
  * Group into batches
  * prefetch data(iterators)
 
