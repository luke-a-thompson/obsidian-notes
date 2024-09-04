A linear transformation (function) $L$ which transforms vectors from one space $V$ to another space $W$. 

For example:
$$
L: V \in \mathbb{R}^{2} \rightarrow W \in \mathbb{R}^{3} \\
$$
$L$ maps a vector $V$ from $\mathbb{R}^2$ to $\mathbb{R}^3$

### Qualities:
**Homogeneity**:
$$
L(c\vec{v}) = cL(\vec{v})
$$For $L$, the product of the [[Scalar Multiplication|scaled vector]] $c\vec{v}$ equals the $c$ times the transformation of the vector, $cL(\vec{v})$.
I.e., [[Scalar Multiplication]] commutes with application of a linear transformation $L$.

**Additivity**:
$$
L(\vec{v} + \vec{w}) = L(\vec{v})+L(\vec{w})
$$The transformation $L$ of the [[Vector Addition|sum of two vectors]] $v,\ w$ is the same as the sum of two transformations of the two vectors.
I.e., [[Vector Addition]] commutes with application of a linear transformation $L$.

### Worked Example
Linear transformations may be represented as matrices.

Consider the transformation:
$$
L: \mathbb{R}^{2} \rightarrow \mathbb{R}^{3},\ L(\vec{v}) = \begin{bmatrix}v_2\\v_1+v_2\\v_1-v_2\end{bmatrix}
$$
Our transformation matrix must transform the standard basis vectors of $\mathbb{R}^{2}$

$$
\begin{align}
\begin{bmatrix}1\\0\end{bmatrix} &= \begin{bmatrix}0\\1+0\\1-0\end{bmatrix} = \begin{bmatrix}0\\1\\1\end{bmatrix} \\
\begin{bmatrix}0\\1\end{bmatrix} &= \begin{bmatrix}1\\0+1\\0-1\end{bmatrix} = \begin{bmatrix}1\\1\\-1\end{bmatrix}\\
\end{align}
$$Therefore, the transformation matrix describing the linear transformation $L$ is:
$$A=\begin{bmatrix}0&1\\1&1\\1&-1\end{bmatrix}$$
To confirm $A\vec{v} = L(\vec{v})$:
$$
A=\begin{bmatrix}0&1\\1&1\\1&-1\end{bmatrix}\begin{bmatrix}v_1\\v_2\end{bmatrix} = \begin{bmatrix}0v_1+1v_2\\1v_1+1v_2\\1v_1-1v_2\end{bmatrix} = \begin{bmatrix}v_2\\v_1+v_2\\v_1-v_2\end{bmatrix}
$$


