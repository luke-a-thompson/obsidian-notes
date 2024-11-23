The *Dirichlet energy* is a functional which measures the smoothness of a function by quantifying the magnitude of its gradient.

For a function $u(x)$ defined on a domain $\Omega \subset \mathbb{R}^{n}$, the Dirichlet energy is:
$$
E[u] = \frac{1}{2} \int_{\Omega}|\nabla u(x)|^2dx
$$Where:
* $|\nabla u(x)|^2$ is the squared gradient magnitude of $u$ at $x$
* $u$ is some function evaluated at $x$
* The integral is performed over the domain of $u$, $\Omega$

## Graph Dirichlet Energy
https://arxiv.org/pdf/2206.10991
The *graph Dirichlet energy* is defined as:
$$
\mathcal{E}^\text{Dir}(F) := \frac{1}{2} \sum_{(i,j)\in E} \|\nabla \mathbf{F}_{ij}\|^2, (\nabla \mathbf{F})_{ij} := \frac{\mathbf{f}_{j}}{\sqrt{d_{j}}} - \frac{\mathbf{f}_{i}}{\sqrt{ d_{i} }}
$$Where:
* $\mathcal{E}^\text{Dir}$ is the graph Dirichlet energy, measuring the smoothness of $\mathbf{F}$
* $\nabla \mathbf{F}$ is the edge-wise gradient of $\mathbf{F} \in \mathbb{R}^{n \times d}$, the node features
* $\mathbf{f}_{i} \in \mathbb{R}^d$ is the feature vector of node $i$
* $d_{i}$ is the degree of node $i$

An equivalent formulation is:
$$
\mathcal{E}^\text{Dir}(F) = \text{trace}(\mathbf{F}^T L \mathbf{F}) = (\text{vec}(\mathbf{F})^T (\mathbf{I}_{d} \otimes \Delta)\text{vec}(\mathbf{F}))
$$Where:
* $\text{vec}(\mathbf{F}) \in \mathbb{R}^{nd}$ is the stacked column vector representation of $\mathbf{F} \in \mathbb{R}^{n \times d}$
* $\otimes$ is the Kronecker product
* The $\text{trace}$ sums the Dirichlet energy contribution across all feature channels
	* $L\mathbf{F}$ encodes the smoothness of each feature across the graph
	* $\mathbf{F}^T (L \mathbf{F})$ contains entries where each diagonal element $(\mathbf{F}^T L \mathbf{F})_{rr}$ is the Dirichlet energy contribution of the $r$-th feature channel across all nodes

### Implications for the Null Space on Graphs
If the Dirichlet energy is set to 0 $\mathbf{F}^T L \mathbf{F}=0$, $L\mathbf{F}$ must be 0 as $L$ is [[Positive Definiteness|positive semi-definite]]. This implies that $\mathbf{F}$ is in the [[Four Fundamental Subspaces#^ec82a0|null space]] of $L$. 

This $\text{Null}(L)$ consists of constant functions as the smallest $\lambda$ of $L$, $\lambda_{0}=0$ has an eigenvector that is constant across all nodes. Thus, in the $\lim_{ \mathcal{E}^\text{Dir}}(\mathbf{F}(t)) \to 0$, the graph function $\mathbf{F}$ takes the same value at each node (constant). This is oversmoothed.

In a continuous function space this produces a harmonic function.