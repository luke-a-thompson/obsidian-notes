Contain a feedback loop
	Hence, even with single input value, can give multiple sequential input values

Unrolled recurrent NN with 2 days of data
* Network 1
	* Input - Day 0 data
	* Input * weight + bias
	* To activation function
	* Activation function output (*w1*)
		* Ignore final output
* Network 2 
	* Input - Network 1 activation function output

Advantages
* Weight, bias same no matter how many times unrolled
	* Hence, number of weights, biases that must be trained does not increase with unrolling

Disadvantages
<https://youtu.be/AsNTP8Kwu80?si=2FfA_UqjeML9DnqE&t=758>
* Exploding gradients
	* If *w1* >1, multiplies each time the network is unrolled
	* E.g. 2 * 2 * 2 * 2 gives *w1* of 16 after 4 unrolls
	* This massive *w1* would mean backpropagation gradient descent would take steps that are too large
	* **Limiting *w1* to <1 produces vanishing gradients**
* 50 sequential inputs of *w1* <1, gradients rapidly approach 0
	* Hence, backpropagation steps too small, and gradient not effectively descended down
* **Solves with LSTMs**
