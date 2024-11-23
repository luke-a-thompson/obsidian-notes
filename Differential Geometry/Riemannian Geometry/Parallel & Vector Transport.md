Consider a Riemannian manifold $M$ with points $p,q \in M$ and tangent spaces $T_{p}M, T_{q}M$. *Parallel transport* and *vector transport* move vector between these two tangent spaces (equivalent to moving vectors along the manifold).
## Parallel Transport
*Parallel transport* $\mathcal{P}$ is the unique linear map that transports vectors along a geodesic:
$$
\mathcal{P}_{p \to q}:T_{p}M \to T_{q}M
$$It computes the entire geodesic path $\gamma(t)$ connecting $p,q$.

It preserves:
* [[Inner Product|Inner Products]]: $\langle v,w \rangle_{p} = \langle \mathcal{P}_{p \to q}v, \mathcal{P}_{p \to q}w \rangle_q$
* Covariant derivatives: $\nabla_{\dot{\gamma}(t)}V(t)=0$
	* $\gamma(t)$ is the [[Geodesic]] from $p$ to $q$
	* $V(t)$ is the parallel transport of $v$ along $\gamma$

**Example:**
Consider a sphere $S^{n}$. For $v \in T_{p}S^{n}$, parallel transport along the geodesic $\gamma$ from $p$ to $q$ is: 
$$
\mathcal{P}*{p \to q}v=v-\frac{\langle v, \dot{\gamma(0)\rangle}}{\|\dot{\gamma(0)}\|^{2}}(q+p)
$$

## Vector Transport
*Vector transport* $\mathcal{T}$ is a more computationally practical approximation (doesn't require differential equations) of parallel transport:
$$
\mathcal{T}*{\eta_{p}}: v \in T_{p}M \to \mathcal{T}*{\eta*{p}} \in T_{q}M
$$
Where:
* $q = \text{Retr}_{p}(\eta_{p})$
* $\eta_{p} \in T_{p}M$ specifies the magnitude and direction of transport
* $n \in T_{p}M$ is the vector being transported

It calculates a tangent vector $\eta_{p}$, moves in this direction, and retracts to $T_{q}M$. This introduces some error in approximating the [[Exponential Map]].

It preserves:
* Associated retraction consistency: $\mathcal{T}_{\eta_{p}}(v) \in T_{q}M$
	* Where $q=\text{Retr}_{p}(\eta_{p})$
	* Ensures transport maps to the correct tangent space
* Zero vector consistency: $\mathcal{T}_{0_{p}}(v)=v$
	* Enforces continuity with the identity map at zero displacement
* Linearity in transported vector: $\mathcal{T}_{\eta_{p}}(\alpha v + \beta w) = \alpha \mathcal{T}_{\eta_{p}}(v) +\beta \mathcal{T}_{\eta_{p}}(w)$
	* 
