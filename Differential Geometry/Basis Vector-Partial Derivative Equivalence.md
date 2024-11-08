Consider the basis vectors $\{\mathbf{e}_{i}\}$ in standard cartesian coordinates:
$$
\{\mathbf{e}_{i}\}=\{\hat{x}, \hat{y}, \hat{z}\}
$$
Then consider a curve $\gamma(t)$ passing through a point $p$. The tangent vector is:
$$
\mathbf{v} = \frac{d\gamma}{dt}
$$In [[Einstein Notation]], this may be equivalently denoted as:
$$
\frac{d}{dt}=\frac{\partial x^{i}}{\partial t}\frac{\partial}{\partial x^{i}}
$$Intuitively,
* $\frac{d}{dt}$ is the total motion along the curve
* $\frac{\partial x^{i}}{\partial t}$ is the amount of movement in *each* coordinate direction (i.e., over a small time)
	* **Recall that Einstein notation means we sum over the directions $x, y$, etc**
* $\frac{\partial}{\partial x^{i}}$ is the direction of movement (i.e., how much things change in just that direction).
	* If it was just $x^{i}$ that would be movement in all directions

Thus, the final equivalence is:
$$
\frac{\partial}{\partial x^{i}} = \mathbf{e}_{i}
$$
