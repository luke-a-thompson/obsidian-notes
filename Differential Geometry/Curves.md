A *curve* $\gamma$ on a manifold $M$ is a smooth $C^\infty$ function from some interval $I \subseteq \mathbb{R}\to M$.

## Velocity
The velocity of a curve $\gamma$ is defined as:
$$
\dot{\gamma}(t) = \frac{d \gamma}{dt}(t)
$$In local coordinates, this is:
$$
\frac{d(x^{i}\circ \gamma)}{dt}\frac{\partial}{\partial x^{i}}
$$
Where:
* $x^{i}$ is the coordinate function in some [[Chart]] $(U, x^{i})$ on $M$
	* In $\mathbb{R}^{3}$, these would be $x^{1}=x$, $x^{2}=y$, $x^{3}=z$
* $x^{i}\circ \gamma$ gives the $i$-th coordinate of the curve using a real valued function: $\mathbb{R}\to\mathbb{R}$
	* In $\mathbb{R}^{3}$ this would be the $x$-coordinate of the path
* $\frac{d(x^{i}\circ \gamma)}{dt}$ is ordinary derivative
	* Each tells us how fast we move in the $i$-th coordinate direction
* $\frac{\partial}{\partial x^{i}}$ is the basis vector
* The sum implied by the Einstein notation gives the velocity vector

See: [[Basis Vector-Partial Derivative Equivalence]]

## Types of Curves
### Local Curves
A *local curve* describes behaviour at some point in a radius $2\epsilon$:
$$
\gamma: (-\epsilon,\epsilon) \to M
$$It is important for defining tangent vector spaces.

## Path Curves
A *path curve* connects two points $\gamma(0)$ and $\gamma(1)$:
$$
\gamma:[0,1] \to M
$$It generally describes parallel transport or [[Geodesic|geodesics]].

## Complete Curves
A *complete curve* is a curve defined for all 'time':
$$
\gamma: \mathbb{R}\to M
$$It generally describes complete geodesics.
