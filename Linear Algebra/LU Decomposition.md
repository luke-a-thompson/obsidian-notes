Less favoured vs [[Cholesky Decomposition]]

# Doolittle Algorithm
## Intuition
**U Matrix**
* We calculate $U$ for each row first
	* Start with the diagonal and move across
	* Easy because L is usefully initialised with $1$s on the diagonal
* We want to compute the value of $U_{ij}$ based on the current row of $A$ and previously computed elements in $L,U$.
* We are saying $U_{ij}=A_{ij}-\text{"contributions from earlier rows"}$


## General Process
1. A matrix $A \in \mathbb{R}^{n \times n}$ can be decomposed into a lower triangular matrix $L$ with $1s$ on the diagonal, and an upper triangular matrix $U$.
2. Iterate over the rows, columns of $A$ to compute $L,u$.
	* For $U$ when $i \leq j$ : $U_{ij} = A_{ij}-\sum_{k=1}^{i-1}\limits L_{ik}U_{kj}$
	* For $L$ when $i > j$ : $L_{ij} = \frac{A_{ij}-\sum_{k=1}^{i-1}\limits L_{ik}U_{kj}}{U_{jj}}$
## Example Calculation
1. We want to decompose the matrix $A$ into the product of two matrices, $L, U$:
$$A = \begin{bmatrix}2&1&1\\4&-6&0\\-2&7&2\end{bmatrix} = LU$$
2. $L,U$ take the form:
$$L = \begin{bmatrix}1&0&0\\L_{21}&1&0\\L_{31}&L_{32}&1\end{bmatrix},\quad U = \begin{bmatrix}U_{11}&U_{12}&U_{13}\\0&U_{22}&U_{23}\\0&0&U_{33}\end{bmatrix}$$
3. To compute $A_{11}$: 
	* $A_{11} = L_{11}U_{11}=1 \times U_{11} = U_{11}$
	* $U_{11} = 2$
4. To compute $U_{12}, U_{13}$
	* $A_{12} = L_{11}U_{12} = 1 \times U_{12}= U_{12}$
	* $U_{12} = 1$

	* $A_{13}= L_{11}U_{13}=1 \times U_{13}= U_{13}$
	* As $A_{13}= 1$, $U_{13} = 1$
5. Hence, the upper triangular matrix U looks like:
	* $\begin{bmatrix}2&1&1\\0&U_{22}&U_{23}\\0&0&U_{33}\end{bmatrix}$
6. To compute $L_{21}, L_{31}$: 
	* $A_{21} = L_{21}U_{11} = L_{21} \times 2$
	* $L_{21} = \frac{A_{21}}{U_{11}} = \frac{4}{2} = 2$ 

	* $A_{31} = L_{31}U_{11} = L_{31} \times 2$
	* $L_{31} = \frac{A_{31}}{U_{11}} = \frac{-2}{2} = -1$
* Hence, the lower triangular matrix L looks like:
	* $\begin{bmatrix}1&0&0\\2&1&0\\-1&L_{32}&1\end{bmatrix}$
7. To compute $U_{22}, U_{23}$:
	* $A_{22} = L_{21}U_{12} + L_{22}U_{22}$
	* $U_{22} = A_{22} - L_{21}U_{12} = -6 - 2 \times 1 = -8$

	* $A_{23} = L_{21}U_{13} + L_{22}U_{23}$
	* $U_{23} = A_{23} - L_{21}U_{13} = 0 - 2 \times 1 = -2$
8. To compute $L_{32}$:
	* $A_{32} = L_{31}U_{12} + L_{32}U_{22}$
	* $L_{32} = \frac{A_{32} - L_{31}U_{12}}{U_{22}} = \frac{7 - (-1 \times 1)}{-8} = \frac{8}{-8} = -1$
9. To compute $U_{33}$:    
	* $A_{33} = L_{31}U_{13} + L_{32}U_{23} + L_{33}U_{33}$
	* $U_{33} = A_{33} - L_{31}U_{13} - L_{32}U_{23} = 2 - (-1 \times 1) - (-1 \times -2) = 1$`
