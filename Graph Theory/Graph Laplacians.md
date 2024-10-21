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
	* Larger $\lambda_1$ suggests good *expansion properties*. Expander graphs remain connected even with edge removal

## Cheeger Inequality
Relates $\lambda_{1}$ to the *conductance* or bottleneckness of a graph.
$$
\frac{\lambda_{1}}{2} \leq \Phi(G) \leq \sqrt{2\lambda_1}
$$Where $\Phi(G)$ is the conductance of a graph $G$ measuring how easily it can be separated into two large components.