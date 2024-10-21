## Aggregation Weights
* Used to combine the predictions of multiple models into a single prediction
* Give more importance to more performant models
* Used in ensemble learning
* Methods - Voting, weighted voting, stacking

### Sparse Tensors
* Tensor with mostly 0s in which only non-zero values are actually recorded (i.e. not all the 0s)
* Saves space / compute when working with sparse data (i.e. data containing many 0s)
## Few-shot Learning
* Model learning from little labelled training data*

## Multi-headed Attention
* Input sequence > multiple heads (representations) > parallel processing > linearly concatenate heads
* Allows network to mix information between pieces of the input sequence

#### Pooling Layer
* Comes after convolutional layer > reduces spatial dimension (width, height) of feature maps while preserving depth (channels)*
* Divide input feature map onto set of non-overlapping pooling regions
* **Summarise presence of features > robustness to changes in feature position in an image, etc("Local Translation Invariance")
* Types
	* Global pooling - Summarises entire feature map into single value

## Data Leakage
* When information from outside the training set is learned by the model
* Invalidates performance estimations

## Permutation Matrix
* Square binary matrix with 1 entry of 1 in each row & column with 0s elsewhere
* <https://www.youtube.com/watch?v=d7AovBKeNMI*>

## Gaussian Elimination
<https://www.youtube.com/watch?v=RgnWMBpQPXk>

## Radial Basis Functions
* Real valued function
* Value dependent on distance between input and a fixed point ("centre")
* Used for interpolation - Finding smooth surface connecting fixed points*

### Intrinsic Mode Functions
* Component of Hilbert-Huang Transform (HHT)
* **Decomposes signal into constituent parts*** - Like a Fourier transform
