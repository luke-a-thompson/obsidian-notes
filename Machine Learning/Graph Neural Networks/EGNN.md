https://arxiv.org/pdf/2102.09844
## Equivariance
If all coordinates $x_{i}$ are *translation equivariant* under a vector $t$, the following must hold:
$$
x_{i}\to x_{i}+t \Rightarrow x_{i}^{l+1} \to x_{i}^{l+1} + t 
$$
Similarly, *rotational equivariance* requires that:
$$
x_{i}\to Rx_{i} \Rightarrow x_{i}^{l+1}\to Rx_{i}^{l+1}
$$
## Architecture
### Node & Coordinate Embedding
Equation 3: $m_{ij}$ represents the message for the edge between nodes $i$ and $j$.
$$
m_{ij}=\phi_{e}(\mathbf{h}_{i}^{l},\mathbf{h}_{j}^{l},\|\mathbf{x}_{i}^{l}-\mathbf{x}_{j}^{l}\|^{2},a_{ij}) \tag{3}
$$Where:
* $\phi_{e}$ is the edge function
* $\mathbf{h}^{l} = \{\mathbf{h}_{0}^{l},\dots,\mathbf{h}_{M-1}^{l}\}$ are the node features at layer $l$
* $\mathbf{x}^{l} =\{\mathbf{x}_{0}^{l},\dots, \mathbf{x}_{M-1}^{l}\}$ are the node coordinates (i.e., $\mathbf{x}^{l}\in \mathbb{R}^{3}$). This yields the relative squared $\ell_{2}$ distance between nodes $i,j$.
	* It is a good idea to use $\ell_{2}$ distances as the basis for edge interactions as they are E(n) equivariant
* $a_{ij}$ are the edge attributes (e.g., bond type)

Equivariance:
* $\|\mathbf{x}_{i}^{l}-\mathbf{x}_{j}^{l}\|^{2}$
	* Equivariant as the **relative** distance cannot change under E(n) perturbations
	* $x_{i}\to x_{i}+t \Rightarrow x_{i}^{l+1} \to x_{i}^{l+1} + t$
	* $x_{i}\to Rx_{i} \Rightarrow x_{i}^{l+1}\to Rx_{i}^{l+1}$

### Coordinate Update
Updates the coordinates $\mathbf{x}_{i}$ of node $i$ based on it's neighbours $\mathcal{N}(i)$.
$$
\mathbf{x}_{i}^{l+1} =\mathbf{x}_{i}^{l}+C\sum\limits_{j\neq1}(\mathbf{x}_{i}^{l}-\mathbf{x}_{j}^{l})\phi_{x}(m_{ij}) \tag{4}
$$Where:
* $\mathbf{x}_{i}^{l}-\mathbf{x}_{j}^{l}$ is the direction vector from node $j$ to $i$
	* Represents direction and distance from $j$ to $i$
	* Used to adjust position of $i$ based on relative position with neighbours. Ensures update sensitive to spatial configuration
	* We use relative distances to remain **equivariant**
* $\phi_{x}(m_{ij})$ is a transformation of $m_{ij}$ controlling how strongly $j$ influences $i$'s position
* $C$ is a constant

Equivariance:
* $\mathbf{x}_{i}^{l}-\mathbf{x}_{j}^{l}$
	* Relative positions unchanged by translation
	* $x_i^l + t + C \sum_{j \ne i} (x_i^l - x_j^l) \, \phi_x(m_{ij}) = x_i^{l+1} + t$
	* $x_i^{l+1} = R x_i^l + C \sum_{j \ne i} R (x_i^l - x_j^l) \, \phi_x(m_{ij})$

Note that the new coordinates $\mathbf{x}_{i}^{l+1}$ are updated based partially on the node features via $m_{ij}$, which in turn depend on the node features $\mathbf{h}_{i}^{l},\mathbf{h}_{j}^{l}$ and relative positions $\|\mathbf{x}_{i}^{l}-\mathbf{x}_{j}^{l}\|^{2}$.
* Chemical explanation? - Atoms with complementary electronic characteristics pulled together?

### Message Aggregation
Equation 5: Performs sum aggregation of the messages from all neighbours of node $i$:
$$
\mathbf{m}_{i}=\sum\limits_{j\neq i}m_{ij} \tag{5}
$$
### Node Embedding Update
Equation 6: The node embedding $\mathbf{h}_{i}^{l+1}$ is updated:
$$
\mathbf{h}_{i}^{l+1} =\phi_{h}(\mathbf{h}_{i}^{l}, \mathbf{m}_{i}) \tag{6}
$$
Where:
* $\phi_{h}$ is the update function applied to the current embedding $\mathbf{h}_{i}^{l}$ and the message $m_{i}$
	* Thus, the new state includes neighbourhood information and node $i$'s own state - duh