The inverse of $A$, $A^{-1}$ such that $AA^{-1}=I$.

### Geometric Intuition
If $A$ is transforms a given space, $A^{-1}$ undoes that transformation. Hence $A^{-1}A=I$ as we perform the transformation, then undo it, returning to the unchanged space (the identity matrix).

### Usefulness in Solving Linear Systems of Equations
A given system of linear equations can be simplified in the following manner:
$$
\begin{align}
Ax &= v \\
A^{-1}Ax &= A^{-1}v \\
x &= A^{-1}v
\end{align}
$$

### Qualities of Invertible Matrices
* All invertible matrices are [[Singular & Degenerate Matrices|non-singular]].
* It's columns show [[Linear Independence]].
* There exists a matrix such that: $$AA^{-1}=I$$
* $Det(A)\neq0$.
	* Why? Because we cannot unsquash a line into a plane

### Process to Calculate $A^{-1}$
