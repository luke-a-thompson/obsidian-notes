## L1 & L2 Norms
### L1 Norm (1-norm, Manhattan norm, taxicab norm):
$$
\begin{align}
\|x\|_1 &= \sum_{i=1}^n\limits|x_{i|}\\
\end{align}
$$
The absolute sum of differences; equal weights to all components.

### L2 Norm (2-norm, Euclidian norm):
$$
\begin{align}
\|u\|_{2} &= \sqrt{\sum_{i=1}^n\limits|x_{i|^2}}\\
\|u\|_{2} &= \sqrt{v^{T}v}\\
\|u\|_{2} &= \sqrt{v \cdot v}
\end{align}
$$
Squaring emphasises larger values.

## Vector Normalisation
A vector $v$ is normalised when $\|v\|=1$.

The [[Inner Product]] of any vector $v$ with $-v$ is the negative square of it's magnitude:
$$
\begin{align}
\text{let}\ v&=\begin{bmatrix}4\\3\end{bmatrix} \\
\|v\| = \sqrt{4^{2}+3^{2}}&=5\\
5^{2}&=25\\
v\cdot(-v) = (4)(-4)+(3)(-3) &= -25
\end{align}
$$


### Orthonormal Vectors
If two vectors $u,\ v$ are normalised ($\|u\| = 1,\ \|v\| = 1$) and orthogonal ($u\cdot v=0$,) they are orthonormal.
