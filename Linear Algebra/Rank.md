The rank of a matrix $A$ is:
1. The number of linearly independent columns and rows. 
2. The dimension of the vector space *spanned* by its columns.

The column and row rank of any matrix are equal.

### Finding the Rank
* The number of non-zero singular values or the number of non-zero elements of $\Sigma$ in the [[Single Value Decomposition]].
* The number of [[pivots]] in [[row echelon form]].
* [[QR Decomposition]] with pivoting.

## Rank Deficiency
### Exact Rank Deficiency
When $\geq1$ columns can be represented as a combination of other columns

if a $3 \times 3$ matrix is of rank 2, the solutions to the system of linear equations it describes are impossible to find or must lie on a plane.
### Numerical Rank Deficiency
When $\geq1$ can be *almost* represented as a combination of other columns due to numerical imprecision.