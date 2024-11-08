A **differentiable** function $f$ has a L-Lipschitz continuous gradient if for some constant $L > 0$ if the following inequality holds:
$$
\|\nabla f(x) - \nabla f(y) \| \leq L \|x -y\|, \forall x,y
$$
I.e., the change in the gradient of $f$ between $x, y$ is bounded by $L$ times the distance between those two points. The ensures $f$ does not change too rapidly, and guarantees a level of "smoothness".

<https://youtu.be/p-8FK2ldGZo?si=EKbYaDVfavUKYlLT>

This gives rise to the following inequality
$$
f(y) \leq f(x) + \langle \nabla f(x),\ y-x \rangle + \frac{L}{2} {\|y-x\|}^2
$$
where $\langle \cdot \rangle$ is the inner product and $\|x\|$ is the L2 norm.
