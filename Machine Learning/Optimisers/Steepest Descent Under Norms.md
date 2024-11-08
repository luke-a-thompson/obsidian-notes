For a function $f: \mathbb{R}^{n}\to \mathbb{R}$, the steepest descent under a norm at a point $x$ is the  direction in which $f(x)$ decreases most rapidly under a unit step of a chosen [[Matrix Norms|norm]] $\|\cdot\|$:
$$
f(x+\alpha d)
$$Where:
* $a$ is the step size
* $\|d\| = 1$ under the chosen norm
## Examples
Given the function $f(x) = x_{1}^{2} + 2x_{2}^{2}$ where $x=(x_{1}, x_{2})$.
$$
\nabla f(x) = \begin{pmatrix}2x_{1} \\ 4x_{2}\end{pmatrix}
$$
$\ell_{2}$-norm
The $\ell_{2}$ norm is the steepest descent under the Euclidean norm:
$$
x_{new}=x-\alpha \begin{pmatrix}2x_{1}\\4x_{2}\end{pmatrix}
$$
$\ell_{1}$ norm
Steepest descent under the $\ell_{1}$ norm maximises the decrease in $f(x)$ per unit $\ell_{1}$-norm. If $|2x_{1}| > |4x_{2}|$:
$$
x_{new}=x-\alpha \begin{pmatrix}\text{sign}(x_{1})\\0\end{pmatrix}
$$It moves in the direction with the largest component of the gradient.
