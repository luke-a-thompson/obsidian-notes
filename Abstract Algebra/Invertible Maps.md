A transformation $f: X \to Y$ is *invertible* or *reversible* and [[bijective]] if there exists a function $f^{-1}:Y\to X$. It is bijective as exactly one element of the codomain $y\in Y$ maps back to one element of the domain $x\in X$.

Invertible functions maintain the *round trip* property which states:
$$
\begin{align}
f^{-1}(f(x)) &= x \space \forall x\ in X \\
f(f^{-1}(y)) &= y \space \forall y \in Y
\end{align}
$$I.e., Applying $f$, then $f^{-1}$ returns $x$. Then applying $f^{-1}$, then $f$, returns to $y$. We can return from the codomain $Y$ to the domain $X$ of the function.

**Example:**
If $\text{f}:X\to Y$, where $f(x) = 2x$, whose inverse is $f^{-1}(x)=\frac{x}{2}$. The round trips are:

For $x_0=3 \in X$:
1. Compute the original function: $f(x_0) = 2(3) = 6$
2. Plug the codomain result into the inverse: $f^{-1}(f(x_0)) = f^{-1}(6) = \frac{6}{2}=3$
For $y_0=6 \in Y$:
1. $f^{-1}(y_0) = f^{-1}(6) = \frac{6}{2} = 3$
2. $f(f^{-1}(y_0)) = f(3) = 2(3) = 6$
