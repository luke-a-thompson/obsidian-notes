A *retraction* on a manifold $M$ is a mapping $R: TM \to M$ satisfying the following properties:

For each $p \in M$, the restriction $R_{p}:T_{p}M \rightarrow M$ satisfies:
1. Centering: $R_{p}(0_{p})$
	* Applying the retraction to $p$ returns $p$ itself
2. Local rigidity: $dR_{p}(0_{p})=\text{id}_{T_{p}M}$
	* The derivative of $R_{p}$ at the zero vector equals the identity map id on the tangent space $T_{p}M$.
## Exponential Map
The *[[Exponential Map]]* is a fundamental example of a retraction defined by the geodesics $v \in T_{p}M$:
$$
\exp_{p}(v) = \gamma_{v}(1)
$$Where $\gamma_{v}$ is the unique geodesic with $\gamma_{v}(0)=p$ and $\gamma_{v'}(0)=v$.
