## Matrix Case
https://www.youtube.com/watch?v=pFKjb9OoUCk
An orthogonal matrix is composed of orthonormal vectors.

### Transformation Interpretation
An orthogonal matrix might be a rotation in space which rotates every vector by $\theta$.
$$R=\begin{bmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{bmatrix}$$
Or it might reflect a vector across the x-axis:
$$R=\begin{bmatrix}1&0\\0&-1\end{bmatrix}$$
### Geometric Interpretation
The columns of an orthogonal matrix represent an **orthonormal** basis for the space. It must be orthonormal, not just orthogonal, to satisfy $A^{T}A=I$.

## Qualities
1. The product of two orthogonal matrices is always orthogonal
2. Preserve the [[Inner Product]]: $(Ai) \cdot (Av)=u \cdot v$
3. Preserve vector norms: $\|Au\|=\|u\|$
	* $\sqrt{(Qu)^{T}Qu} = \sqrt{u^{T}Q^{T}Qu} = \sqrt{u^{T}u}$
4. Preserve angles between vectors - All 2D [[Rotation Matrices]] are orthogonal
5. $A^{T}= A^{-1}$
	* This is true of any matrix that satisfies $A^{T}A=I$
6. $A^{T}A=I$ because it's columns are rows are orthonormal vectors
7. $Det(A) = \pm 1$