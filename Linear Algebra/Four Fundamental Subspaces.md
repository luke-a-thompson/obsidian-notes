Consider a matrix $A \in \mathbb{R}^{m \times n}$.

### Column Space / Image
The column space of $A$ denoted $Col(A)$ is the set of all vectors that can be expressed as a linear combination of the columns of $A$. Hence, **it is the rank of the matrix.**
$$
Col(A) = \{Ax:x \in \mathbb{R}^{n} \}
$$
### Null Space / Kernel

^ec82a0

The null space of $A$ denoted $\text{Null}(A)$ is the set of all vectors $x \in \mathbb{R}^{n}$ such that $Ax=0$. The dimension of the null space is the *nullity* of $A$.

The *rank-nullity theorem* states that for a matrix $A \in \mathbb{R}^{m\times n}$:
$$
\text{rank}(A)-\text{nullity}(A)=n
$$
### Row Space / Coimage
The row space of $A$ denoted $Row(A)$ is the subspace of $\mathbb{R}^{n}$ spanned by the rows of $A$ that contains all possible linear combinations of the rows of $A$.

### Left Null Space / Null Space of $A^{T}$
The set of all vectors $y = \mathbb{R}^{m}$ such that $A^{T}y= 0$. Hence, it is the set of all vectors in $\mathbb{R}^{m}$ that are mapped to the zero vector in $\mathbb{R}^{n}$ when multiplied by $A^{T}$. The dimension of the left null space is the *co-nullity*.
Equivalent to the column space of $A^{T}$.

## Qualities
* The dimensions of the row space and dimensions of the column space and rank are equal: $dim(Row(A)) = dim(Col(A)) = rank(A)$
* The sum of the dimensions of the null space and row space is the column count: $dim(Null(A)) + dim(Row(A)) = n$
* The sum of the dimensions of the left null space and column space is the row count:  $dim(Null(A^{T})) + dim(Col(A)) = m$
