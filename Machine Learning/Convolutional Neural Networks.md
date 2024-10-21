## Convolution
### Locality, Aggregation & Composition
* Performed on each pixel
* Locality
	* Receptive field of mask - Capture area centred on a pixel
	* Enables invariancy to location of feature in image
* Aggregation
	* Multiply mask coefficients with all pixels inside mask > aggregate sum > replace value of centre pixel
* Composition
	* Occurs over multiple layers
	* Combine simple features (e.g. edges, texture) > combine to represent complex patterns

* **Convolution operation**
	* Slide a kernel ("filter") across input data > element-wise multiplication > sum
		* Multiple usually used - Allows learning / detection of different features from single input
	* Produces a *feature map* - Spatial map of features detected by kernel
	* See also: [[Terms#Stride]]
* Filters - Small matrices of weights learned during training > extract features from input data
### Stride
* In CNNs - Number of pixels by which the mask or filter is moved across the input image 
	* Larger stride >small output size
	* Can downsample input & reduce dimensionality - Esp. in pooling & convolutional layers
	* Usually 1 or 2 (1 means filter moves 1 pixel at a time & would maintain dimensionality)
