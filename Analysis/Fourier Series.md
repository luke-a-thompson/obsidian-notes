A **periodic function** $f(x)$ can be represented as a sum of $\sin, \cos$ waves of increasingly high frequency:
$$
f(x) = \frac{A_{0}}{2}+\sum_{k=1}^\infty\Bigl(A_{k}\cos(kx)+B_{k}\sin(kx)\Bigl)
$$Where:
* $\frac{A_{0}}{2}$ is a constant: Non-oscillatory component
* $A_{k}, B_{k}$ are Fourier coefficients determining the amplitude of the $k$-th $\cos, \sin$ waves
* $\cos(kx),\sin(kx)$ are the oscillatory components of $f(x)$
	* $k$ is a multiplier on the fundamental frequency. For a $2\pi$-periodic function this is: $f_{1}= \frac{1}{2\pi}$
	* **The $k$-th term in the Fourier series $\cos(kx)$ or $\sin(kx)$ corresponds to a frequency that is $k$ times the fundamental frequency: $f_{k}=k\cdot f_{1}= \frac{k}{2\pi}$**
	* E.g., if $k=3$. there would be $3$ cycles in $2\pi$

This works as a function approximation if we sum to a finite value.

**Example:**
Considering a function $f(x) \in L_{2}\bigl([0,L)\bigl)$ which is [[Square-Integrable]] in the space of [[Lebesgue Integrable Functions]] (i.e., the inner product of $\langle f(x),f(x)\rangle$ is bounded). We can write the Fourier series as:
$$
\frac{A_{0}}{2}+\sum_{k=1}^\infty \Bigl(A_{k}\cos(\frac{2\pi kx}{L})+B_{k}\sin(\frac{2\pi kx}{L})\Bigl)
$$We use a periodicity of $L$ as $f(x)$ is defined between $[0,L)$.
## Computing Fourier Constants
The *Fourier coefficients* are computed as the [[Hilbert Space]] [[Inner Product|inner products]] between $f(x)$ and the $\sin, \cos$ waves:
$$
\begin{align}
A_{k}=\frac{1}{\pi}\int_{-\pi}^\pi f(x)\cos(kx)dx = \frac{1}{\lvert \cos(kx) \rvert^2 } \langle f(x), \cos(kx) \rangle \tag{1} \\
B_{k}=\frac{1}{\pi}\int_{-\pi}^\pi f(x)\sin(kx)dx = \frac{1}{\lvert \sin(kx) \rvert^2 } \langle f(x), \sin(kx) \rangle \tag{2}
\end{align}
$$The inner product must be normalised by the "length" of $\cos(kx)$. This is like considering the waves as orthogonal basis directions in a vector space.