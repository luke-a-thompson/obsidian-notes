In the following notation, min is because the number of singular values is equal to the smaller of $m$ and $n$.

## Nuclear Norm

^ca2b21

The *nuclear norm* of a matrix $A$ is the sum of singular values $\sigma$:
$$
\|A_{m\times n}\|_{*} = \sum\limits_{i=1}^{\text{min}(m,n)}\sigma_{i}
$$
This is the matrix analogue of the $l_{1}$ norm. Works as a convex version of the $\text{rank}(\cdot)$ function so is easy to minimise in optimisation problems.
## Frobenius Norm

^116450

The *Frobenius norm* of a matrix $A$ is the square root of the sum of squares of its elements, or equivalently the sum square signular values:
$$
\|A_{m \times n}\|_{F} = \sqrt{\sum_{i=1}^{m}\limits \sum_{j=1}^{n}\limits|a_{ij}|^{2}} = \sqrt{\sum\limits_{i=1}^{\text{min}(m,n)}\sigma^{2}_{i}}
$$
This is the matrix analogue of the [[Vector Norms#L2 Norm (2-norm, Euclidian norm)|L2 norm]] when considering the columns of $A$ as a vector:
$$
\left\|\begin{bmatrix}1&-2&0\\-1&3&2\\1&-1&1\end{bmatrix}\right\|_{F}
=
\|\begin{bmatrix}1\\-1\\1\\-2\\3\\-1\\0\\2\\1\end{bmatrix}\|_2
$$
## Spectral Norm

^d53a60

The spectral norm of a matrix $A$ is the largest singular value $\sigma$:
$$
\|A\|_{\infty}=\max_{i}\sigma_{i}
$$

## Schatten $p$-Norm
The *Schatten $p$-norm* of a matrix $A$ is:
$$
\|A_{m\times n}\|_{p} = \left(\sum\limits_{i=1}^{r}\sigma_i^{p} \right)^{1/p}
$$Where $\sigma_i$ are the singular values of $A$ and $p \in \mathbb{R},\ p > 1$.

It generalises norms by interpolating between different measures of matrix size. 
* When $p=1$: Nuclear norm $\sum_{i=1}^{\min(m,n)} \sigma_i$
* When $p=2$: Frobenius norm $\|A\| = \left( \sum_{i=1}^{\min(m,n)} \sigma_{i}^{2} \right)^{1/2} = \|A\|_{F}$
* When $p=\infty$: Spectral norm $\|A\|=\max_{i}\sigma_{i}$
	* By showing only the largest $\sigma$, it bounds how much $A$ can stretch a vector $v$ in $\mathbb{R}^{d}$.

### Duals of Schatten $p$-Norms
The *dual* of a *Schatten* $p$-norm is the Schatten $q$-norm where:
$$
\frac{1}{p} + \frac{1}{q}=1
$$
The duals of common schatten norms are:
* $p=1, q=\infty$: Dual nuclear norm $\|A\|_{S_{\infty}} = \max_{i}\sigma_{i}$ is the spectral norm

**Special cases**
* Schatten 1-norm is the [[Matrix Norms#^ca2b21|nuclear norm]]
* Schatten 2-norm is the [[Matrix Norms#^116450|Frobenius norm]]
* Schatten $\infty$-norm is the [[Matrix Norms#^d53a60|spectral norm]]
