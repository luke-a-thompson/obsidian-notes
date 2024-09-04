A unit vector is a vector whose length is 1.
$$u \cdot u = 1$$
To produce a unit vector $u$ in the same direction as a vector $v$:
$$u = \frac{v}{\|v\|}$$
This is termed *normalisation*.

Due to the [[Cauchy-Schwartz Inequality]] the dot product of any two unit vectors is always $\le 1$.

**Examples:**
Consider a plane with two unit vectors $j=(0,1)$ and $i=(1,0)$. For the vector $v = (1,1)$, the unit vector is:
$$
\begin{align}
\|v&\| = \sqrt{\begin{bmatrix}1\\1\end{bmatrix} \cdot \begin{bmatrix}1\\1\end{bmatrix}} = \sqrt{2} \\
\\
u& = \begin{bmatrix}\frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}}\end{bmatrix}
\end{align}
$$
