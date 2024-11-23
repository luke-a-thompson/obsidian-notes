The *expectation* $\mathbb{E}$ of a random variable $X$ is the average outcome of infinitely repeated samplings of that random variable.

For discrete random variables this is expressed as:
$$
\mathbb{E}[X] = \sum\limits_xx\cdot P(X=x)
$$
Hence, the expectation of $X$ equals the sum of each possible value $x$ times the probability of the draw from $X$ being $x$.

For continuous random variables this is expressed as:
$$
\mathbb{E}[X]=\int_{-\infty}^{\infty}x\cdot f(x)dx
$$Where:
* $x$ is each possible value $X$ could take
* $f(x)$ is the PDF
* $dx$ indicates we are integrating w.r.t $x$, summing over all $x$ values.
Hence, $x\cdot f(x)$ means we multiply each possible value by its probability density.

## Online & Offline Expectation
**Offline**
Known distribution, exact expectation:
$$
\begin{align}
\text{Discrete: }\mathbb{E}[X] &= \sum\limits_xx\cdot P(X=x)\\
\text{Continuous: }\mathbb{E}[X]& = \int_{-\infty}^{\infty}x\cdot f(x)dx
\end{align}
$$
**Online**
Sequential observations, continually updated. Running averages are typical:
$$
\hat{\mu}*{n}=\frac{1}{n}\sum\limits*{i=1}^{n}x_i
$$
