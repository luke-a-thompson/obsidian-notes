A permutation matrix has a $1$ in every row and column. All other elements are $0$.

### Types
**Partial pivoting** - Change the rows of $A$ (the order of equations).
**Complete pivoting** - *Also* change the order of the columns (the order of the variables).

### Examples
The order of a $2\times2$ matrix $A$ is $\{1,2\}$. It's permutation matrix $P$ is the identity matrix $I$.
$$
\begin{bmatrix}1&2\\2&1\end{bmatrix} \begin{bmatrix}1&0\\0&1\end{bmatrix} = \begin{bmatrix}1&2\\2&1\end{bmatrix}
$$
**Row Permutation**
Right multiply the permutation matrix, $PA$:
$$
\begin{bmatrix}0&1\\1&0\end{bmatrix}\begin{bmatrix}a&b\\c&d\end{bmatrix}  = \begin{bmatrix}c&d\\a&b\end{bmatrix}
$$
**Column Permutation**
Left multiply the permutation matrix $AP$:
$$
\begin{bmatrix}a&b\\c&d\end{bmatrix} \begin{bmatrix}0&1\\1&0\end{bmatrix} = \begin{bmatrix}b&a\\d&c\end{bmatrix}
$$

If you are pivoting you don't need to pivot the last column