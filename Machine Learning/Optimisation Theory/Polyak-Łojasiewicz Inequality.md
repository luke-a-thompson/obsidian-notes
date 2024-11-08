The *Polyak-Łojasiewicz (PL) inequality* aka *gradient dominance condition* guarantees the convergence of gradient-based optimisation algorithms on a non-convex function $f(\theta)$.

For a function $f: \mathbb{R}^{d} \to \mathbb{R}$ with minimum value $f^{*}$, the PL inequality states:
$$
\frac{1}{2}\|\nabla f(\theta)\|^{2}\geq \mu(f(\theta)-f^{*})
$$Where:
* $\theta$ are the paramaters
* $\nabla f(theta)$ is the gradient of $f$ at $\theta$
* $\mu > 0$  is a constant depending on the properties of $f$

The PL inequality ensures that if $\nabla f$ is large, $f(\theta)$ is far from its minimum $f^{*}$. It does not require convexity, yet still guarantees linear convergence with appropriate step-size.

NNs often satisfy PL-like conditions locally (Karimi, et al. 2016).
