## First Order - Gradient
*First order* methds only use the gradient of the loss function w.r.t the parameters.

Properties:
* Fast, memory efficient
* Struggle with curavture, saddle points, plateaus

**Examples:**
1. SGD
2. Adam (approximate second order)

## Second Order - Gradient & Hessian
*Second order* methods use the gradiant and Hessian of the loss function

Properties:
* Computationally expensive or intractible for high-dimensional models
* Better curvature, more accurate updates & often convergence

**Examples:**
1. Newton's
2. L-BFGS
3. Adam (approximate)
	* EMA of squared gradients approximates variance > gives local curvature via approximation of the diagonal Hessian
