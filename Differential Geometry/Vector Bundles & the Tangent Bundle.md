A *vector bundle* consists of two manifolds:
* Base space: $M$
* Total space: $E$
* Projection: A $C^\infty$ surjective map $\pi:E \to M$
Such that for each point $p \in M$, the *fibre* $\pi^{-1}$ is a vector space.

## Properties
* Bundle rank: The dimension of the fibre $\pi^{-1}(p)$ is constant across all points $p \in M$
* The [[Group Structure]] is typically $GL(n, \mathbb{R}$)

## Types of Bundles
### Tangent Bundle $TM$
The *tangent bundle* $TM$ of a $C^\infty$ manifold $M$ is a vector bundle defined as:
$$
TM = \bigcup_{p\in M}T_{p}M
$$Each fibre $T_{p}M=\pi^{-1}(p)$ is the tangent space at $p$.

It also contains:
* The *total space*: All tangent vectors at all points of $M$: $E=TM$
* A smooth projection $\pi:TM \to M$ mapping each tangent vector to its base point

**Properties**
* $\dim(TM) = 2\dim(M)$
### Cotangent Bundle
The *cotangent bundle* is dual to the tangent bundle and is equipped with a metric $g^{*}$ induced by $g$. It houses the exterior derivative and differential forms.

### Frame Bundle
