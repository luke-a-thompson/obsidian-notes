The *exponential map* $\exp_{x}:T_{x}\mathcal{M} \to \mathcal{M}$ at a point $x$ on a [[Riemannian Manifold]] $\mathcal{M}$ is a function mapping a tangent vector $v \in T_{x}M$ to a point on $\mathcal{M}$. It is a specific case of [[Retractions & The Exponential Map]]

## Calculation

Define a [[Geodesics|geodesic]] equation on $\mathcal{M}$ with [[Riemannian Metric]] $g$. The geodesic curves $\gamma(t)$ must satisfy:
$$
\frac{D}{dt}\dot{\gamma}(t)=0
$$Where:
* $\frac{D}{dt}$ is the [[Covariant Derivative]] along $\gamma$
* $\dot{\gamma}(t)$ is the tangent vector $\gamma$ at $t$

Solve (usually numerically) the geodesic equation with the initial conditions:
1. $\gamma(0)=x$
2. $\dot{\gamma}(0)=v$

Evaluate at $t=1$: Once $\gamma(t)$ is found, $\exp_{x}(v)$ is given by the position $\gamma(1)$.

The *exponential map* of a point $p$ on a Riemannian manifold $M$ is an $n$-dimensional vector space formed of the span of the partial derivatives viewed as tangent vectors at $p$.
