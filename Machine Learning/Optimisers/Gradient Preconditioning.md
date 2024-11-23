*Preconditioned gradient descent* modifies the optimisation geometry by incorporating a [[Positive Definite Matrices|positive definite matrix]] $P$:
$$
\min_{\Delta w}g^T\Delta w+ \frac{1}{2\eta}\|\Delta w\|_{P}^2
$$Where:
* $g$ is the gradient vector $\nabla J(w)$ at the parameter $w$
* $\Delta w$ is the update step for $w$
* $\eta$ is the learning rate
* $\|\Delta w\|_{P}^{2} = \Delta w^{T}P\Delta w$ is squared generalised norm of the update step
	* $P$ is a [[Positive Definite Matrices|positive semi-definite matrix]] [[Induced & Operator Norm|inducing the norm]]
	* Produces a scalar as $w$ is a vector

## Example Cases of $P$
When $P=I$, it induces the $\ell_{2}$ [[Vector Norms#^dbb1fb|Euclidian norm]]:
$$
\|\Delta w\|_{I}^2 = \Delta w^T I \Delta w = \|\Delta w\|_{2}^2
$$
When $P = \text{diag}(p_{1},p_{2},\dots,p_{d})$, the induced norm scales each component of $\Delta w$ by $\sqrt{ p_{i} }$:
$$
\|\Delta w\|_{P}^2 = \Delta w^TP\Delta w = \sum_{i=1}^d p_{i}(\Delta w_{i})^2
$$
When $P=H,\ H=\nabla^2J(w)$, where $H$ is the [[Hessian]] of the loss function the induced norm reflects the curvature of the loss landscape:
$$
\|\Delta w \|_{H}^2 = \Delta w^T H\Delta w
$$

To convert the above squared-norms into the induced norms just square root the quadratic form.