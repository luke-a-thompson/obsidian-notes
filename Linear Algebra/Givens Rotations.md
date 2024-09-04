A 2D rotation in the plane which zeroes specific elements of a matrix or vector. $G(i, j, \theta)$ is an identity matrix with a $2\times2$ rotation matrix in the coordinates $(i, j)$.

### Process:
Suppose we have a vector or matrix $A = \begin{bmatrix}a\\b\end{bmatrix}$ and we want to zero the second element, $b$.

1. Calculate the *hypotenuse* or rotation angle $r$.
$$
r = \sqrt{a^{2}+ b^{2}}
$$
2. Find the cosine of $\theta$:
$$
c = \frac{a}{r}
$$
3. Find the sine of $\theta$:
$$
s = \frac{-b}{r}
$$
4. Form the Givens rotation matrix $G$:
$$
G = \begin{bmatrix} 1 & & & & & & \\ & \ddots & & & & & \\ & & c & s & & & \\ & & -s & c & & & \\ & & & & \ddots & & \\ & & & & & 1 & \end{bmatrix}
$$
Finally, apply $G$ by multiplying the vector by $G$ on the left
$$
G \cdot A
$$

**Example**:
Consider the vector $\vec{x} = \begin{bmatrix}4\\3\end{bmatrix}$. 
Calculate the rotation.
$$
r = \sqrt{4^{2}+ 3^{2}} = 5
$$
Then calculate the sine and cosine
$$
\begin{align}
c &= \frac{4}{5} = 0.8 \\
s &= \frac{-3}{5} = 0.6
\end{align}
$$
Now form and apply the Givens rotation matrix $G$:
$$
\begin{align}
G &= \begin{bmatrix}0.8 & -0.6 \\ 0.6 & 0.8\end{bmatrix} \\
G \cdot \mathbf{x} &= \begin{bmatrix} 0.8 & 0.6 \\ -0.6 & 0.8 \end{bmatrix} \begin{bmatrix} 4 \\ 3 \end{bmatrix} = \begin{bmatrix} (0.8 \times 4) + (0.6 \times 3) \\ (-0.6 \times 4) + (0.8 \times 3) \end{bmatrix} = \begin{bmatrix}3.2+1.8\\-2.4+2.4\end{bmatrix} = \begin{bmatrix}5\\0\end{bmatrix}
\end{align}
$$

### Use in the [[QR Decomposition]]
### Forming the $Q$ matrix

1. Each Givens rotation $G_{i}$ is orthogonal. Hence, $G_{i}^{T}=G_{i}^{-1}$
	* The product of orthogonal matrices is also orthogonal*
### Forming the $R$ matrix:
1. Iteratively apply givens rotations to zero out elements below the diagonal.
$$
R = \begin{bmatrix}
r11&r12&r13&r14\\
r21&r22&r23&r24\\
r31&r32&r33&r34\\
r41&r42&r43&r44\\
\end{bmatrix}
$$
Example order of rotations
1. Rotate $r41$ with $r31$
2. Rotate $r31$ with $r21$
3. Rotate $r21$ with $r11$
* Formally, this is: $R=G_{k}G_{k+1}G_{k}\dots G_{k11}A$. 
* Now, elements below the diagonal are $0$, and the diagonal is the final rotation.

