The Rayleigh quotient for a given [[Hermitian Matrices & Tranpose|Hermitian matrix]] $M^{n}$ and non-zero vector $x$ is:
$$R(M,x) = \frac{x^{*}Mx}{x^{*}x}$$
If $(\lambda, v)$ is an eigenpair (satisfies $Av=\lambda v$), then:
$$r(v) = \frac{v^{*}Av}{v^{*}v} = \frac{\lambda v^{*}v}{v^{*}v} = \lambda$$
For and $x^{n}$:
$$\lambda_{1} \leq r(x) \leq \lambda_{n}$$
To get the eigenvalue corresponding to an eigenvector, substitute $x$ for that eigenvector.

### Generalised Rayleigh Quotient
For a pair of matrices $A$ and $B$ and a non-zero vector $x$, the generalised Rayleigh quotient is:
$$R(A,B;x):=\frac{x^{*}Ax}{x^{*}Bx}$$
This may be reduced to the standard Rayleigh quotient via:
$$R(C^{-1}AC^{*-1},C^{*}x)$$
where $CC^{*}$ is the [[Cholesky Decomposition]] of the [[Hermitian Matrices & Tranpose|Hermitian]] [[Positive Definiteness|positive definite]] matrix $B$.