This paper seeks to understand classical GNNs in an optimisation framework with a minimiser and a regulariser.

<https://arxiv.org/pdf/2101.11859>

## Conceptualising GNNs in an Optimisation Framework
GNNs generally aim to achieve two goals:
1. Encode useful information from the features
2. Utilise the smoothing capability of graph topology

We can formulate this as:
$$
\mathcal{O} = \min_Z \{ \underbrace{\zeta \|\mathbf{F}_1 \mathbf{Z} - \mathbf{F}_2 \mathbf{H}\|_F^2}_{O_{\text{fit}}} + \underbrace{\xi \, \text{tr}(\mathbf{Z}^T \tilde{\mathbf{L}} \mathbf{Z})}_{O_{\text{reg}}}\}

$$
Where:
* $\zeta, \xi$ are constants $>0$. $\zeta$ is usually $[0,1]$
* $\mathbf{H}$ is a transformation of the original input feature matrix $X$
* $\mathbf{F}_{1}, \mathbf{F}_{2}$ are arbitrary graph convolution kernels
* $\mathbf{Z}$ is the final propagation result when minimising the objective $\mathcal{O}$

We are finding the best $\mathbf{Z}$ which minimises the objective $\mathcal{O}$.
### $\mathcal{O}_{fit}$
$$
{\zeta \|\mathbf{F}_1 \mathbf{Z} - \mathbf{F}_2 \mathbf{H}\|_F^2}
$$Find a $\mathbf{Z}$ that is close to the initial feature representation $\mathbf{F}_{2}\mathbf{H}$. I.e., one that captures feature information well.

### $\mathcal{O}_{reg}$
$$
\xi \ \text{tr}(\mathbf{Z}^{T \tilde{\mathbf{L}} \mathbf{Z})}= \frac{\xi}{2}\sum\limits_{i,j}^{n}\hat{\tilde{A}}_{ij}\|\mathbf{Z}_{i}-\mathbf{Z}_{j}\|^{2}
$$Find a $\mathbf{Z}$ that encourages graph smoothness by penalising differences in features $\mathbf{Z}$ across connected nodes $i,j$. This is equivalent to minimising the [[Dirichlet Energy]] of the graph. Low Dirichlet energy allows the GNN to capture the homophily of the graph.
