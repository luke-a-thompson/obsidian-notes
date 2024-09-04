The $QR$ matrix decomposition decomposes a matrix $A$ into the product of an orthonormal basis $Q$ and $R$, the transformation coefficients to return to $A$.
## General Process
1. For a matrix $A \in \mathbb{R}^{k \times k}$ initialise the $Q,R \in \mathbb{R}^{k \times k}$. The vectors contained are denoted $a_{k},q_{k},r_{k}$
2. Set $q_{1}$ to $\frac{a_{1}}{\|a_{1}\|}$ and $r_{kk}=\|a_{1}\|$
3. For $k>1$, compute projections $r_{ik} = q_{i}^{T}a_k$
4. Subtract the projections from $v_{k}=a_{k} - \sum_{i=1}^{k-1}\limits r_{ik}a_{k}$
	* $v_{k}$ is the orthogonalised but unnormalized $a_{k}$
5. $r_{kk} = \|v_{k}\|$ becomes, and $q_{k}=\frac{v_{k}}{r_{kk}}$
	* To return to $a_k$, we could do: $r_{kk}q_{k} + \sum_{i=1}^{k-1}\limits r_{ik}a_{k}$ to get $v_{k}$, by returning to the unnormalised $v_{k}$ with $r_{kk}q_{k}$, then re-adding the other vectors.
## Methods
1. [[Gram-Schmidt]]
2. [[Gram-Schmidt#Modified Gram-Schmidt]]
3. [[Householder Reflection]]
4. [[Givens Rotations]]

A = QR then R @ Q yields a [[Similar Matrices]] matrix with the same eigenvalues of A

Determinant of QR equal to plus/minus 1 <https://math.stackexchange.com/questions/575380/relationship-between-eigenvector-values-and-qr-decomposition>
<https://www.andreinc.net/2021/01/25/computing-eigenvalues-and-eigenvectors-using-qr-decomposition>
