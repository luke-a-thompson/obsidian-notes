In the following notation, min is because the number of singular values is equal to the smaller of $m$ and $n$.

### Nuclear Norm
The nuclear norm of a matrix $A$ is :
$$
\|A\|_{*} = \sum\limits_{i=1}^{\text{min}(m,n)}\sigma_{i}
$$
The sum of the singular values.
Matrix analogue of the $l_{1}$ norm. Works as a convex version of the rank function so is easy to minimise in optimisation problems.
### Frobenius Norm
The Frobenius norm of a matrix $A$ is:
$$
\|A_{m \times n}\|_{F} = \sqrt{\sum_{i=1}^{m}\limits \sum_{j=1}^{n}\limits|a_{ij}|^{2}} = \sqrt{\sum\limits_{i=1}^{\text{min}(m,n)}\sigma^{2}_{i}}
$$
This is the square root of the sum of the squares of its elements. Equivalently the sum of the squares of the singular values.

This can also be thought of as the [[Vector Norms#L2 Norm (2-norm, Euclidian norm)|L2 norm]] of the columns of $A$ as a vector:
$$
\left\|\begin{bmatrix}1&-2&0\\-1&3&2\\1&-1&1\end{bmatrix}\right\|_{F}
=
\|\begin{bmatrix}1\\-1\\1\\-2\\3\\-1\\0\\2\\1\end{bmatrix}\|_2
$$