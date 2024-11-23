## Dot Product
The the *dot product* of $v=(v_{1}, v_{2})$ and $w=(w_{1,}w_2)$ is computed as:
$$v \cdot w = v_{1}w_{1} + v_{2}w_{2}$$
Equivalently, in matrix form this is:
$$v^{T}w = \begin{bmatrix}v_1&v_2\end{bmatrix}\begin{bmatrix}w_1\\w_2\end{bmatrix} = v_1w_1+v_2w_2$$

The **sign** of the dot product of two vectors $v \cdot w$ indicates the angle the two vectors make.
* If $v \cdot w < 0$, the [[Cosine Angle]] is $<90\degree$
* if $v \cdot w = 0$, the [[Cosine Angle]] is $0\degree$ and the vectors are orthogonal
* If $v \cdot w > 0$, the [[Cosine Angle]] is $>90\degree$
* Generally, the dot product increases as the vectors overlap more and more
	![[Pasted image 20240630004552.png]]


### Qualities
* The dot product of vectors obeys the [[Cauchy-Schwartz Inequality]].
* The line $y=4x$ is orthogonal to $y=-\frac{1}{4}x$.

### Using Slopes to Determine Orthogonality
If the product of the slopes of $v=\begin{bmatrix}1\\2\end{bmatrix}$ and $w=\begin{bmatrix}-2\\1\end{bmatrix}$ is -1, they are orthogonal.