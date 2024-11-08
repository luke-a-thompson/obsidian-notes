Consider a Riemannian manifold $M$ with points $p,q \in M$ and tangent spaces $T_{p}M, T_{q}M$. *Parallel transport* and *vector transport* move vector between these two tangent spaces (equivalent to moving vectors along the manifold).
## Parallel Transport
*Parallel transport* $\mathcal{P}$ is the unique linear map that transports vectors along a geodesic:
$$
\mathcal{P}_{p \to q}:T_{p}M \to T_{q}M
$$
It preserves:
* Inner products: $\langle v,w \rangle_{p} = \langle \mathcal{P}_{p \to q}v, \mathcal{P}_{p \to q}w \rangle_q$
* Covariant derivatives: $\nabla_{\dot{\gamma}(t)}V(t)=0$
	* $\gamma(t)$ is the [[Geodesic]] from $p$ to $q$
	* $V(t)$ is the parallel transport of $v$ along $\gamma$

**Example:**
1. Consider a sphere $S^{n}$. For $v \in T_{p}S^{n}$, parallel transport along the geodesic $\gamma$ from $p$ to $q:\mathcal{P}_{p \to q}v=v-\frac{\langle v, \dot{\gamma(0)\rangle}}{\|\dot{\gamma(0)}\|^{2}}(q+p)$

## Vector Transport
*Vector transport* $\mathcal{T}$ is a more computationally practical approximation of parallel transport
