The *induced norm* aka *operator norm* is the biggest stetching a linear transformation can apply to a vector $x$.

Consider a linear transformation $L: \mathbb{R}^{n} \to \mathbb{R}^{m}$, letting $A \in \mathbb{R}^{m\times n}$ be it's matrix representation. The *induced norm* of this linear transformation is:
$$
\|A\| = \sup_{x\neq 0} \frac{\|L(x)\|}{\|x\|} = \sup_{x\neq 0}\frac{\|L\frac{x}{\|x\|}\|}{\frac{x}{\|x\|}}
$$

They are "induced" because they are in part determined by the vector norms $\|x\|$ chosen for the input and the output.
