The *induced norm* aka *operator norm* is the biggest stretching a [[Linear Transformations|linear transformation]] can apply to a vector $x$.

Consider a linear transformation $L: \mathbb{R}^{n} \to \mathbb{R}^{m}$, letting $A \in \mathbb{R}^{m\times n}$ be it's matrix representation. The *induced norm* of this linear transformation is:
$$
\|A\| = \sup_{x\neq 0} \frac{\|L(x)\|}{\|x\|} = \sup_{x\neq 0}\frac{\|L\frac{x}{\|x\|}\|}{\frac{x}{\|x\|}}
$$

They are "induced" because they are in part determined by the [[Vector Norms]] $\|x\|$ chosen for the input and the output.
They are "operator" norms because they are caused by a linear operator $A$.

**Example:**
Consider the $\ell_{1}$ operator norm $1,i$:
$$
\|A\|_{1, i}=\sup_{x\neq0}\frac{\|Ax\|_{1}}{\|x\|_{1}}
$$The right hand side induces the $\ell_{1}$ norm because we chose it.

## Induced Norm of a [[Riemannian Manifold]]
A Riemannian manifold $\mathcal{M}$ can induce a norm via its [[Riemannian Metric]] $g$, which defines an inner product $g_{x}(u,v)$ on the tangent space $T_{x}M\ \forall x\in M$:
$$
\|v\|_{x} = \sqrt{ g_{x}(v,v) }
$$