## Diffeomorphism to $\mathbb{R}^{3}$
For any point $x\in \mathcal{M}$ on a manifold $\mathcal{M}$ there a neighbourhood $U$ around $x$ within $\mathbb{R}^d$ and an open set $V \subseteq \mathbb{R}^d$. This is a [[Diffeomorphism]] $\psi:U \to V$ such that:
$$
\psi(\mathbf{U} \cap \mathcal{M}) = \mathbf{V} \cap E \in \mathbb{R}^d
$$Where:
* $\psi$ is a diffeomorphism assigning each point in $U \cap M$ to a corresponding point in $V$
	* **Translates curved structure of $\mathcal{M}$ within $U$ to a linear, coordinate-based view in $V$**
* $U \cap \mathcal{M}$ is the portion of $U$ on the manifold $\mathcal{M}$
* $V \cap E$ is the image of $U \cap \mathcal{M}$ in $V$, restricted to lie in $E$
* $E$ is a linear subspace and $\text{dim}(n)=\text{dim}(\mathcal{M})$
![[Pasted image 20241114235311.png]]
## Tangent Vectors and Spaces
### Tangent Vector
A *tangent vector* at $x$ is at the velocity $c'(0) = \lim_{ t \to 0 } \frac{c(t)-c(0)}{t}$ of a [[Curves|curve]] $c:\mathbf{R} \to \mathcal{M}$ with $c(0)=x$. I.e., There is a smooth curve on $\mathcal{M}$ that passes through $x$ with velocity $v$.

### Tangent Space
The *tangent space* $T_{x}M$ is the set of all tangent vectors of $\mathcal{M}$ at $x$. It is a linear subspace of $\mathcal{E}$, with the same dimension of $\mathcal{M}$.

If a surface were not a manifold (i.e., it were a non smooth X shape), the tangent space formed of tangent vectors would not be linear.
![[Pasted image 20241115000404.png]]