### Assumptions
* Data can be modelled by a tilted, stretched Gaussian

Not robust to anisotropic noise
Can capture "almost" linearly dependent features
## Robust PCA
Useful when there is anisotropic or correlated noise - "salt and pepper noise"
Robust to outliers

Splits the data $X = LS$:
* $L$ Eigenfaces - Low-rank components well described by PCA
* $S$ Sparse matrix - A sparse matrix of outliers not described by the eigenfaces

**How it works**
$X = LS$ is ill-posed and underdetermined
* There are infinite ways to factor a matrix into two other matrices
* However, this is "solvable" if a regularisation penalty is added to push us towards a good solution.
* $min \textbf{ rank}(L) + \|S\|_{0}$  where $\|S\|_{0}$ denotes the $L0$ norm of $S$ so that $L+S=X$
	* Problem: Neither [[Rank]] nor 0-norm are convex. Hard to optimise.
	* Relaxed to convex via $min\text{ } \|L\|_{*} + \lambda \|S\|_{1}$, where $\|L\|$ is the [[Matrix Norms#^ca2b21]] and $\lambda \|S\|_{1}$ is the 1-norm (the sum of absolute values) of S
	* Trained on a bunch of normal faces
