*Regularised gradient descent* or *proximal gradient descent* is written as:
$$
\min_{\nabla w}g^{T}\Delta w+ \frac{1}{2\eta}\|\Delta w\|_{2}^{2}
$$Where:
* $g$ is the gradient vector $\nabla J(w)$ at the parameter $w$.
* $\Delta w$ is the update step for $w$
* $\eta$ is the learning rate
* $\|\delta w\|_{2}^{2}$ is the squared $L^{2}$-norm of the update step - **Regularisation**

The regularisation penalises large steps to prevent overshooting. This is useful when the function is non-linear or sharp.
