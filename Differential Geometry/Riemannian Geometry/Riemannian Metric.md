The *Riemannian metric* is on a differentiable manifold $M$ is a smoothly-varying [[Inner Product]] defined on the tangent space $T_{p}M$ at each point $p \in M$. For each $p$ the metric provides:
$$
g_{p}: T_{p}M \times T_{p}M \to \mathbb{R}
$$where $g_{p}$ assigns a real values inner product to any pair of tangent vectors at $p$.

As $g$ varies smoothly across each $p \in M$, calculations in $T_{p}M$ can consistently reflect the local curvature of the manifold.

It induces metrics on associated [[Vector Bundles & the Tangent Bundle|vector bundles]].
## Smoothness Condition
The Riemannian metric $g$ varies **smoothly** across $M$. Thus, if $X,Y$ are smooth vector fields on $M$, the Riemannian metric $g(X,Y)$ is also smooth. Mathematically, we require that the function:
$$p\mapsto g_p​(X_p​,Y_p​)$$
is smooth (i.e., $C^\infty$) for all smooth vector fields $X,Y$ on $M$. At each point $p \in M$, the vector fields $X$ and $Y$ define tangent vectors $X_p, Y_p \in T_pM$ in the tangent space at $p$. 

If we take two nearby points $p,q \in M$, the inner products $g_p(X_p,Y_p)$ and $g_q(X_q,Y_q)$ will be similar, since the vector fields $X,Y$ and metric $g$ vary smoothly.

## Other Conditions
1. The metric $g$ is symmetric: $g_{p}(X,Y) = G_{p}(Y,X)$ for all vector fields $X,Y$
2. The metric is [[Positive Definiteness|positive definite]]: $g_{p}(X,X)>0$ for all nonzero $X\in T_{p}M$
3. $g$ varies smoothly w.r.t $p$ and the vector fields

## Local Coordinates
