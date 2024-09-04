Used for solving systems of linear equations $Ax = b$ where $A$ is large & sparse.

## Krylov Subspace
The Krylov subspace $K$ of order m of matrix $A$ with the vector v equals the span of a series of $Av$. It consists of all linear combinations of the vectors $v,Av,A^{2}v,\dots, A^{m}v$.
$$
K_{m(A,v)} = \text{span}(v,Av,A^{2}v,\dots, A^{m}v)
$$
If A is $n \times n$, $K$ has $\leq n$ dimensions. $K_m$ must be contained in $K_{m+1}$ because $K_{m+1}$ includes an additional basis vector $A^{m+1}v$ beyond those in $K_M$ . Hence:
$$K_{m} \subseteq K_{m+1} \subseteq \cdots \subseteq K_{M}$$
Multiplying each vector in the Krylov space $K_M$ by $A$ shifts the basis vectors up by a power of $A$. This is because each application of $A$ expresses $v$ in a new basis formed by the action of $A$. $A^{2}$ is just like applying $A$ twice. We are successively transforming $v$ by $A$.
$$AK_{M} = \text{span}(v,Av,A^{2}v,\dots, A^{m}v) \subseteq K_{M+1} = K_M$$
This occurs because $K_{M}$ already captures all the relevant directions in the vector space.

### Example
Consider a matrix $M \in \mathbb{R}^{2 \times 2}$ and a vector $v \in \mathbb{R}^{2}$:
1. $K_{1} = \text{span}(v)$
2. $K_{2} = \text{span}(v, Av)$
3. $K_{3} = \text{span}(v, Av, A^{2}v) = \text{v, Av}$
4. Hence, $K_{3}=K_{2}$ and $K_{M+1}=K_{M}$ for $M \geq 2$.
	* This is because the vector space is 2D, and Krylov spaces cannot grow beyond the idmension of the space they are in.
