The *weak* and *strong solutions* are two notations of solving an equation depending on its regularity.

## Strong Solutions
A function $u$ is a strong solution to a PDE if:
1. $u$ belongs to a function space where all derivatives required by the PDE exist and are continuous
2. $u$ satisfies the PDE everywhere in the domain

Such solutions often exist when the data is smooth, and the domain has regular properties. They don't always exist.

**Example:**
For the [[Laplace's & Poisson's Equations#^a601c7|Poisson equation]] $-\Delta u=f$ in $\Omega$ with boundary conditions $u=g$ on $\partial \Omega$, the strong solution $u$ satisfies:
1. $u \in C^2(\Omega)$: The Laplacian $\Delta u$ is well-defined
2. $u$ satisfies $-\Delta u=f$ pointwise in $\Omega$ 

## Weak Solutions
A function $u$ is a weak solution to a PDE if:
1. $u$ belongs to a weaker function space (e.g., $H^1(\Omega)$, the [[Sobolev Space]] of square-integrable functions with square-integrable first derivatives)
2. $u$ satisfies the PDE in a weak form, derived by integrating the PDE against a test function $\phi \in C_{0}^\infty(\Omega)$ (smooth, compact support)

**Example:**
For the [[Laplace's & Poisson's Equations#^a601c7|Poisson equation]] $-\Delta u=f$ in $\Omega$ with boundary conditions $u=g$ on $\partial \Omega$, the weak solution $u$ satisfies:
1. Multiply the PDE by a test function $\phi$ and integrating:
$$
\int_{\Omega}\nabla  u \cdot \nabla \phi dx = \int f \phi dx,\forall \psi \in H_{0}^1(\Omega)
$$