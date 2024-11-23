## Interpreting the Eigendecomposition of the Graph Laplacian
The eigendecomposition of the graph Laplacian for a graph $G=(V,E)$ is:
$$
L\mathbf{v}_{i}= \lambda_{i}\mathbf{v}_i
$$Where $\lambda_{i}$ is the $i$-th eigenvalue of $L$ and $\mathbf{v}_i$ is the corresponding eigenvector. $\mathbf{v}_{i}$ is of dimension $|V|$.

Each component $\mathbf{v}_{i}[j]$ of $\mathbf{v}_{i}$ corresponds to node $j$, so the $j$-th entry of $\mathbf{v}_{i}$ tells the value of $j$ in the embedding associated with $\lambda_{i}$. **This is the coordinate of the node in the spectral embedding.** 

**Spectral Clustering**
* Construct the *spectral embedding* $U$ - Take the first $k$ eigenvectors (corresponding to the smallest non-zero $\lambda$)
	* $U = [\mathbf{v}_{1}, \mathbf{v}_{2}, \dots, \mathbf{v}_{k}]$, $U \in \mathbb{R}^{|N|\times k}$
* Treat each row of $U$ as a feature vector of the corresponding node, apply clustering algorithms

## Unnormalised Graph Laplacian
Captures the difference between local connectivity $A$ and node's degree $D$.
$$
L=D-A
$$**Properties**
* Symmetric if graph is undirected
* Smallest $\lambda > 0$ corresponds to number of connected components in the graph

## Normalised Graph Laplacian
Accounts for node degrees by scaling the adjacency matrix $A$ and the degree matrix $D$.

**Symmetric Normalised Laplacian**$$
L_{sym} = I-D^\frac{-11}{2}AD^\frac{-1}{2}
$$
**Random-Walk Normalised Laplacian**
$$
L_{rw}=I-D^{-1}A
$$
Where $D^{-1}A$ are the *transition probabilities* of moving from node $i$ to node $j$, normalised by $\delta_{i}$ and $\delta_{j}$. 

**Properties**
* Reduces bias introduced by high-$\delta$ nodes
* The spectral gap $\lambda_{1}- \lambda_{0} = \lambda_{1}$ as $\lambda_{1}=0$ for connected graphs defines algebraic connectivity
	* Larger $\lambda_{1}$ denotes a more connected graph, harder to separate into communities; small $\lambda_{1}$ suggests clustering and easy partitioning with few cuts
	* Larger $\lambda_1$ suggests good *expansion properties*. [[Expander graphs]] remain connected even with edge removal

## Graph Frequencies
The *frequencies* of a graph are the [[Eigenvectors & Eigenvalues|eigenvalues]] $\lambda_{0} \leq \lambda_{1} \leq \dots \leq \lambda_{n-1}$ of the graph Laplacian $L$. They provide a spectral decomposition describing how functions vary across the graph structure.

**Measuring Frequency Components of a Node**
The *spectral coefficient* of a function $f$ (e.g., node feature vectors) is computed as the dot product between $f$ and the $i$-th eigenvector of $L$:
$$
f_{i}=\langle f, u_{i} \rangle
$$Where:
* $f_{i}$ is the spectral coefficient of the function $f$
	* It is the contribution of the $i$-th graph frequency $\lambda_{i}$ to $f$
	* A large $f_{i}$ would indicate a significant component of the graph frequency $\lambda_{i}$
* $u_{i}$ is the $i$-th eigenvector of the graph Laplacian $L$


Smaller $\lambda$ correspond to low frequencies which vary slowly across the graph, while larger $\lambda$ correspond to rapidly varying high frequencies.

## Cheeger Inequality
Relates $\lambda_{1}$ to the *conductance* or bottleneckness of a graph.
$$
\frac{\lambda_{1}}{2} \leq \Phi(G) \leq \sqrt{2\lambda_1}
$$Where $\Phi(G)$ is the conductance of a graph $G$ measuring how easily it can be separated into two large components.
