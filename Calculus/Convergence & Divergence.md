## Convergence
If a series is *convergent*, the sequence of [[Partial Sum|partial sums]] approaches a finite limit:
$$
\lim_{n\rightarrow \infty}S_{n}=L
$$Where $L \in \mathbb{R}$.

**Example:**
Consider the series $\sum\limits_{n=1}^{\infty}\frac{1}{2^{n}}$ and its partial sum:
$$
\begin{align*}
S_1 &= \frac{1}{2} = 0.5 \\
S_2 &= \frac{1}{2} + \frac{1}{4} = 0.75 \\
S_3 &= \frac{1}{2} + \frac{1}{4} + \frac{1}{8} = 0.875 \\
S_4 &= \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \frac{1}{16} = 0.9375 \end{align*}
$$This partial sum converges to $1$, so $\lim_{n \rightarrow \infty}S_{n}=1$. As $n$ approaches $\infty$, the sum of all $n$ elements approaches $1$.

## Divergence
If a series is *divergent*, the limit of the [[Partial Sum|partial sum]] is infinite or non-existent (oscillates, etc):
$$
\lim_{n \rightarrow \infty}S_{n}= \infty
$$
**Example:**
Consider the series $\sum\limits_{n=1}^{\infty}\frac{1}{n}$:
$$
\begin{align*}
S_1 &= 1 \\
S_2 &= 1 + \frac{1}{2} = 1.5 \\
S_3 &= 1 + \frac{1}{2} + \frac{1}{3} \approx 1.83 \\
S_4 &= 1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} \approx 2.08
\end{align*}
$$
This partial sum keeps growing unbounded, so $\lim_{n \rightarrow \infty}S_{n}=\infty$. As $n$ approaches $\infty$, the sum of all $n$ elements approaches $\infty$.

**Non-existent Example:**
Consider the series $\sum\limits_{n=1}^{\infty}(-1)^n$:
$$\begin{align*} S_1 &= -1 \\
S_2 &= -1 + 1 = 0 \\
S_3 &= -1 + 1 - 1 = -1 \\
S_4 &= -1 + 1 - 1 + 1 = 0
\end{align*}
$$This partial sum oscillates between -1 and 0, so $\lim_{n \rightarrow \infty}S_{n}$ does not exist. As $n$ approaches $\infty$, the sum of all $n$ elements continues to alternate between these two values, never settling on a limit.

TODO:
Ratio test
Comparison test