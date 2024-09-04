Recall that all reflection $R$ matrices are [[Orthogonality#Matrix Case|orthogonal]] as $R^{T}R=I$.

Householder reflections construct a matrix $H$ which transforms a vector $x$ into another vector $u$ that is parallel to a coordinate axis. H takes the form:
$$H = I-2uu^{T}$$
This makes all but one element $0$.

Because Householder matrices are always orthogonal, their product is also orthogonal. Hence their use in [[QR Decomposition]].
### Process
1. Define a vector $x$ and a target vector $e_1$ of the form $(\|x\|, 0, \dots, 0)$:
$$
x=\begin{bmatrix}4\\3\end{bmatrix},\ e_1=\begin{bmatrix}1\\0\end{bmatrix}
$$
2. Find $\|x\|$:
$$
\|x\|=\sqrt{4^{2}+3^{2}} = 5
$$
3. Determine the vector $v$ such that the Householder reflection $H$ maps $x$ to $-\|x\|e_1$. First find $u$:
$$
\begin{align}
\|x\|e_{1} &= 5\begin{bmatrix}1\\0\end{bmatrix} = \begin{bmatrix}5\\0\end{bmatrix} \\
u &= x-\|x\|e_{1}= \begin{bmatrix}4\\3\end{bmatrix} - \begin{bmatrix}5\\0\end{bmatrix} = \begin{bmatrix}-1\\3\end{bmatrix}
\end{align}
$$
4. Normalise $u$ to get $v$:
$$
\begin{align}
\|u\| =\sqrt{-1^{2}+3^{2}}=\sqrt{10}\\
v = \frac{u}{\|u\|} = \begin{bmatrix}\frac{-1}{\sqrt{10}}\\\frac{3}{\sqrt{10}}\end{bmatrix}
\end{align}
$$
5. From $v$ form the householder matrix, $H$:
$$
\begin{align}
H &= I - 2\frac{vv^T}{v^Tv}\\
vv^{T}&=\begin{bmatrix}\frac{-1}{\sqrt{10}}\\\frac{3}{\sqrt{10}}\end{bmatrix} \begin{bmatrix}\frac{-1}{\sqrt{10}}&\frac{3}{\sqrt{10}}\end{bmatrix} = \begin{bmatrix}\frac{1}{10} & -\frac{3}{10}\\-\frac{3}{10}&\frac{9}{10}\end{bmatrix}\\
v^{T}v &= \begin{bmatrix}\frac{-1}{\sqrt{10}}&\frac{3}{\sqrt{10}}\end{bmatrix}\begin{bmatrix}\frac{-1}{\sqrt{10}}\\\frac{3}{\sqrt{10}}\end{bmatrix} = \frac{1}{10}+\frac{9}{10} =1 \\
\\
H &= I-2 \frac{\begin{bmatrix}\frac{1}{10} & -\frac{3}{10}\\-\frac{3}{10}&\frac{9}{10}\end{bmatrix}}{1} = \begin{bmatrix}1-\frac{2}{10}&\frac{6}{10}\\\frac{6}{10}&1-\frac{18}{10}\end{bmatrix} = \begin{bmatrix}0.8&0.6\\0.6&-0.8\end{bmatrix}
\end{align}
$$
6. Apply $H$ to $x$
$$
Hx = \begin{bmatrix}0.8&0.6\\0.6&-0.8\end{bmatrix} \begin{bmatrix}4\\3\end{bmatrix} = \begin{bmatrix}3.2+1.8\\2.4-2.4\end{bmatrix} = \begin{bmatrix}5\\0\end{bmatrix}
$$
The resulting vector $\begin{bmatrix}5\\0\end{bmatrix}$ is aligned with $e_1$.
