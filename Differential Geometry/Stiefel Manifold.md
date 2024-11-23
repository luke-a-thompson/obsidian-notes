The *Stiefel manifold* $\text{St}(n,p)$ where $n \geq p$ is the set of all ordered $p$-tuples of [[Orthogonality|orthonormal]] vectors in $\mathbb{R}^n$. Equivalently, it is the set of all $n \times p$ matrices with $V$ orthonormal columns.
$$
\text{St}(n,p) = \{ V \in \mathbb{R}^{n\times p}: V^TV=I_{p} \}
$$
## Properties
* The dimension of $\text{St}(n,p)$ is: $\text{dim St}(n,p)=np- \frac{p(p+1)}{2}$
* The [[Principal Bundle]]: $\text{St}(n,p) \to \text{Gr}(n,p)$ forms a principle $O(p)$ bundle
* Special cases
	* When $p=1$: $\text{St}(n,1) = S^{n-1}$
	* When $p=n$: $\text{St}(n,n) = O(n)$ the orthonormal [[Groups|group]]

## Metric
The [[Riemannian Metric]] on $\text{St}(n,p)$ is induced from the Frobenius inner product:
$$
\langle A,B \rangle_{F} = \mathrm{Tr}(A^TB)
$$