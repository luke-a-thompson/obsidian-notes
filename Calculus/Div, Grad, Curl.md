Consider a scalar field $f(x,y,z)$. The div, grad and curl operators perform the following transformations:
$$
\text{Scalar field }f \rightarrow \text{vector field } \nabla F \rightarrow \text{scalar field } \nabla^{2}F
$$
The nabla operator $\nabla$ is a vector of partial derivatives
## Grad $\nabla$
The grad operator $\nabla$ takes a scalar field $f(x,y,z)$ and converts it to a vector field:
$$
\nabla f=\begin{bmatrix}\frac{\partial f}{\partial x}\\\frac{\partial f}{\partial y}\\\frac{\partial f}{\partial z}\end{bmatrix}
$$This tells the gradient of the function at each point with respect to each direction of the scalar field $f$.

**Example:**
Consider a temperature field $f(x,y,z) = x^{2}+2y-z$:
$$
\nabla f = \begin{bmatrix} \frac{\partial f}{\partial x} \\ \frac{\partial f}{\partial y} \\ \frac{\partial f}{\partial z} \end{bmatrix} = \begin{bmatrix} 2x \\ 2 \\ -1 \end{bmatrix}
$$Here, we have taken the partial derivatives with respect to each component of the scalar field.

At point $(1,0,0)$
$$
\nabla f = \begin{bmatrix}2\\2\\-1\end{bmatrix}
$$

## Div $\nabla^{2}$, the Laplacian
Recall the notation for second derivatives
$$
\frac{\partial}{\partial x} \left(\frac{\partial T}{\partial x} \right) = \frac{T}{dx \cdot dx} = \frac{\partial^{2}T}{\partial x^{2}}
$$The $^{2}$ appears in the numerator denotes that differentiation was performed twice. The $^{2}$ in the denominator is showing that $dx$ was divided by twice.

**Div vs Laplace operator**
* The div operator $\nabla \cdot$ takes a vector field $F(x,y,z)$ and produces a scalar field.
	* $\text{div } F = \nabla \cdot F = \frac{\partial Fx}{\partial x} + \frac{\partial Fy}{\partial y} + \frac{\partial Fz}{\partial z}$
* The Laplace operator $\nabla^{2}$ takes a scalar field and produces a scalar field.
	* $\nabla^{2} = \frac{\partial^{2}}{\partial x^{2}} + \frac{\partial^{2}}{\partial y^{2}} + \frac{\partial^{2}}{\partial z^2}$

**The Laplacian specifically operates on spatial coordinates.** Hence, in the [[Heat Equation]], it results in a partial derivative with respect to spatial coordinates $x$, not time $t$.

^d58b6a
**Example:**
$$
\nabla^{2} = \nabla \cdot (\nabla f) = \begin{bmatrix} \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \end{bmatrix} \cdot \begin{bmatrix} \frac{\partial f}{\partial x} \\ \frac{\partial f}{\partial y} \\ \frac{\partial f}{\partial z} \end{bmatrix} = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2}
$$The matmul here means we are taking the second derivative of each component of the original scalar field. We are dotting the nabla operator with a pre-existing scalar field.
