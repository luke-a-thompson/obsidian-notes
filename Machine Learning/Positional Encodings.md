## Connection between Graph Laplacian PE and Conventional PE
Consider the input sequence to a LLM as a *path graph* $G$ of $N$ tokens where each token is a node, and consecutive tokens are connected by edges.

The eigenvalues $\lambda_k$ and eigenvectors $v_k$ of the Laplacian $L$ of this path graph can be represented as $\sin$ and $\cos$ terms.

For a path graph with $N$ nodes, the eigenvalues and eigenvectors are:
$$
\begin{align}
\lambda_{k}&= 2-2\cos\left(\frac{k\pi}{N+1}\right), &k \in \{1,2,\dots N\}\\
v_{k(i)}&= \sin(\frac{ki\pi}{N+1}), &i \in \{1,2,\dots,N\}, k \in \{1,2,\dots N\}
\end{align}
$$
$N+1$ is required to account for the Dirchlet boundary condition.
