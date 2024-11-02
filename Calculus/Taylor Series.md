A function $f(x)$ may be *Taylor expanded* about a base point $a$ (if $f$ is infinitely differentiable at $a$) via:
$$
f(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \cdots
$$We want $x$ to be as close to $a$ as possible.

In numerical methods when studying perturbations to a system $f(x+\Delta x)$ , the Taylor series is:
$$
f(x+\Delta x) = f(x) + \frac{df}{dx}(x)\cdot \Delta x+ \frac{d^{2}f}{dx^{2}}(x)\cdot \frac{\Delta x^{2}}{2!} \cdots+ \frac{d^{n}f}{dx^{n}}(x)\cdot \frac{\Delta x^{n}}{n!}
$$Here, the $\Delta x$ plays **the same role** as the $x-a$ in the first expression.

When $\Delta x \ll 1$ or, equivalently, when $x-a$ is small as $x$ is close to $a$, each successive Taylor polynomial becomes much smaller than the previous as squaring a number $<1$ shrinks it. Hence, less expansions are required as these terms shrink.

## Maclaurin Series
When a Taylor series is expanded about a base point $a=0$, it is a *Maclaurin series*.
Consider the function $f(x) = \sin(x)$ with $a=0$:
$$
\begin{align}
f(x) &= \sin(0) + \cos(0)\cdot x + \frac{-\sin(0)}{2!}x^{2}+\frac{-\cos(0)}{3!}x^3+\cdots\frac{f^{(n)}(0)}{n!}x^{n}\\
&= 0+x-\frac{1}{3!}x^{3}+\frac{1}{5!}x^{5}\cdots
\end{align}
$$Notice that we only have the odd terms as $\sin(0)$ is $0$. Also notice that the signs alternate.