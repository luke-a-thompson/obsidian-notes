A matrix $A$ is similar to $B$ if an [[Matrix Inverse|invertible]] matrix $P$ exists such that:
$$B = P^{-1}AP$$
$P$ represents a change of basis between the vector spaces of $A$ & $B$.

Thus, $A$ and $B$ necessarily represent the same [[Linear Transformations|linear transformation]] or system of equations, just with respect to different bases.
### Qualities of Similar Matrices
1. **Same [[Eigenvectors & Eigenvalues|eigenvalues]]**.
	* If $Bx = M^{-1}AMx = \lambda x$, then $AMx = \lambda Mx$. Accomplished by multiplying both sides by $M$.
	* So they have the same eigenvalues, but different eigenvectors. M changes the eigenvectors, they were originally $x$.
1. Same [[Determinant]], [[Trace]] & [[Rank]]
