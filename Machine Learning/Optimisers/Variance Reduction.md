*Variance reduction* is a technique to stabilise an optimisation process by reducing the noise of gradient estimates. 

### Stochastic Variance Reduced Gradient (SVRG)
https://papers.nips.cc/paper_files/paper/2013/file/ac1dd209cbcc5e5d1c6e28598e8cbbe8-Paper.pdf
SVRG is described by:
$$
\hat{\nabla }=\nabla f_{i}(x_{t})-\nabla f_{i}(\tilde{x})+\tilde{\mu}
$$Where:
* $\tilde{x}$ is the snapshot (anchor) point
* $\tilde{\mu}$ is the full gradient at snapshot $\tilde{x}$
	* **Must be periodically reset with full gradient**
* $x_{t}$ is the current parameter value at iteration $t$
* $\nabla f_{i}(x_{t})$ is the gradient of the $i$-th sample at the current point
* $\nabla f_{i}(\tilde{x})$ is the gradient of the $i$-th sample at the snapshot

### SARAH & SPIDER Recursive Gradient Differencing
https://arxiv.org/abs/1807.01695
SARAH & SPIDER:
$$
\begin{align}
v_{t} &= \nabla f(x_{t},\xi_{t})-f(x_{t-1}\xi_{t})+v_{t-1} \\
x_{t+1} &= x_{t} - \eta_{t}v_{t}
\end{align}
$$Where:
* $v_{t}$ is the variance reduced gradient at iteration $t$ or $v_{t-1}$: Combines current, past information
	* **Must be periodically reset with full gradient**
* $x_{t}$ is the current parameter vector
* $\xi_{t}$ is the current random sample
* $\nabla f(x_{t},\xi_{t})$ is the gradient at the current point 
* $\nabla f(x_{t-1}\xi_{t})$ is the gradient at the previous point, using same minibatch sample

**Properties:**
* $\mathbb{E} \|v_{t}-\nabla f(x_{t})\|^2$ decreases over time, as $t$ gets bigger
	* The variance-reduced estimates gets closer to the true gradient over time (SGD constant)
* Recursive accumulation of variance-reduced gradient
* $\nabla f(x_{t},\xi_{t})-f(x_{t-1}\xi_{t})$ captures local geometry

### Stochastic Recursive Momentum (STORM)
STORM:
$$
\begin{align}
\mathbf{m}_t &= \beta_1\mathbf{m}_{t-1} + (1-\beta_1)[\nabla f(\mathbf{x}_t,\xi_t) + \frac{\beta_1}{1-\beta_1}(\nabla f(\mathbf{x}_t,\xi_t) - \nabla f(\mathbf{x}_{t-1},\xi_t))] \\
\mathbf{x}_{t+1} &= \mathbf{x}_t - \alpha_t\mathbf{m}_t
\end{align}

$$Where:
* $\mathbf{m}_t$ is the momentum term at step $t$
* $\mathbf{x}_t$ is the parameter vector at step t
* $\beta_{1}$ is a momentum coefficient
* $\alpha$ is the learning rate
* $\nabla f(\mathbf{x}_{t}, \xi_{t})$ is a minibatch gradient sample
* $\xi_{t}$ is a random sampling of the data at step $t$
* $\frac{\beta_1}{1-\beta_1}$ is a correction factor on the momentum
	* As $\beta_{1}$ approaches 1, the gradient update is increased