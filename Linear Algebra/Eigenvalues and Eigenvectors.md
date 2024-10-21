## Stability

## Eigendecomposition
A matrix $A^{n \times n}$ can be factorised as:
$$A=Q \Lambda Q^{-1}$$
Where $Q$ is a $n \times n$ matrix of eigenvectors, and $\Lambda$ is the diagonal matrix of eigenvalues.

The decomposition is derived from the [[Fundamental Theory of Eigenspaces]]:
$$
\begin{align}
Av &= \lambda v \\
AQ &= Q \Lambda \\
A &= Q \Lambda Q^{-1}.
\end{align}
$$
The linearly independent eigenvectors with non-zero eigenvalues form a basis for all possible $Ax$

### Qualities
1. Only possible for [[diagonalisable matrices]]
2. Known as a *spectral decomposition* when the matrix is [[Normal Matrices|normal]] or [[Symmetric Matrices|symmetric]].