The eigenvalues of a matrix $A^{n\times n}$ are scalars $\lambda$ satisfying $Av = \lambda v$, where $v$ is an eigenvector. They are computed using the characteristic equation $\text{det}(A-\lambda I) = 0$.
## Eigenvalue Multiplicity
#### Algebraic Multiplicity
* The number of times $\lambda$ appears as a root of the [[Characteristic Polynomial]]: $det(A - \lambda I) = 0$.
	* E.g., If the characteristic polynomial was $p(\lambda) = (\lambda - 2)^{2}(\lambda  -3) = 0$, the multiplicity of $\lambda = 2$ is $2$.
	* This is a *repeated root*.
#### Geometric Multiplicity
* Recall: Any $\lambda$ can have multiple associated eigenvectors which all lay in $\text{null}(A-\lambda I) = (A-\lambda I)\mathbf{v} = 0$
* The number of linearly independent eigenvectors associated with $\lambda$.
	* Example
		* Consider the matrix $A = \begin{bmatrix}4&1&0\\0&4&0\\0&0&5\end{bmatrix}$
		* For the eigenvalues $\lambda = 4$, perform $(A-4I)$: $A-4I=\begin{bmatrix}0&1&0\\0&0&0\\0&0&1\end{bmatrix}$
		* Solve for $\text{Null}(A) = (A-4I)\mathbf{v} = 0$ (this is also the eigenspace of $\lambda = 4$), 
			* Where $\mathbf{v} = \begin{bmatrix}v_{1}\\v_{2}\\v_{3}\end{bmatrix}$ is the eigenvector
			* This gives the equation: $\begin{bmatrix}0&1&0\\0&0&0\\0&0&1\end{bmatrix}-\begin{bmatrix}v_{1}\\v_{2}\\v_{3}\end{bmatrix} = 0$
			* For each row
				* $0 \cdot v_{1} + 1 \cdot v_{2} + 0 \cdot v_{3}= 0 \implies v_{2}=0$
				* $0=0$
				* $0\cdot v_{1} + 0 \cdot v_{2} + 1 \cdot v_{3}=0 \implies v_{3}=0$
		* As $v_{1}$ doesn't appear in any equation, it is **free**
			* Think about it: Even if $v_{1}=20$, $\begin{bmatrix}0&1&0\\0&0&0\\0&0&1\end{bmatrix} \begin{bmatrix}20\\0\\0\end{bmatrix} = \begin{bmatrix}0\\0\\0\end{bmatrix}$
		* So $\lambda = 4$ has a geometric multiplicity of $1$ because there is only 1 linearly independent eigenvector 

## Properties for [[Symmetric Matrices]] (i.e., [[Graph Laplacian]])
* The eigenvectors of symmetric matrices are orthogonal
* Sign ambiguity
	* If the eigenvector $v$ of matrix $L$ has the eigenvalue $\lambda$, and scalar multiple $kv$ is also associated.
	* As the scalar can be $-1$, there is sign ambiguity.
	* In LSPE GNNs, this is resolved by SignNet.
* Basis ambiguity
	* If the [[Eigenvectors & Eigenvalues#^f4f034|geometric multiplicity]] $>1$ then the dimensionality of the eigenspace $>1$ and any linearly independent vectors spanning this space can serve as a valid basis.
	* Hence, different algorithms may produce different eigenvectors (i.e., different bases) for the same eigenspace $(A-\lambda I)\mathbf{v}$.
	* In LSPE GNNs, this is resolved by BasisNet.
* Algebraic multiplicity = geometric multiplicity for all $\lambda$.

**Left and right eigenvectors**
The left eigenvector $u$ of $A$ corresponding to $\lambda$ is:
$$
Au=\lambda u
$$
The right eigenvector $v$ of A corresponding to $\lambda$ is:
$$
A^{T}v=\lambda v
$$
## Relation to [[Singular Values]]
$\lambda$ of $A^{T}A$ or $AA^{T}$ are the squared singular values $\sigma^{2}$ of $A$.
* Identically, $\sigma = \sqrt{\lambda}\text{ of }A^{T}A$.
* Hence, they are always $>0$.
* **They are not the $\sigma^{2}$ of A**.

**Key differences**
* $\sigma$ describe the action of $A$ on all vectors, $\lambda$ only describe the action of $A$ on eigenvectors.
* $\sigma$ are always $>0$, $\lambda$ may be negative or complex.
* $\sigma$ apply to any matrix, $\lambda$ are only defined for square matrices.
* $\sigma$ are derived from $A^{T}A$ (always [[Positive Definite Matrices|positive semi-definite]], $\lambda$ are derived from $A$ directly.


## Stability
(<https://youtu.be/XXjoh8L1HkE?si=AU8AFWpe4pQEFgzn>)

If a matrix $A$ is perturbed $A+\epsilon E$ , the condition $\kappa(\lambda)$ number of each eigenvalue $\lambda$ determines how much the eigenvalues $A$ change in response.

The condition number of an eigenvalue $\lambda$ of $A$ is:
$$
\kappa(\lambda) = \frac{1}{v^{H}u}
$$Where
* $u$ is a right eigenvector of $A$ corresponding to $\lambda$
* $v$ is a left eigenvector of $A$ corresponding to $\lambda$
* $v^{H}u$ is the inner product of $v$ and $u$
