*Adam* is a (diagonally) [[Gradient Preconditioning|preconditioned]] [[Stochastic Gradient Descent|gradient descent]] algorithm incorporating adaptive per-parameter scaling and momentum accumulation.

## Moment Estimation
Adam maintains two moment estimates for the gradients:
**First moment (mean)**:
$$\begin{align}
m_{t} &= \beta_{1}m_{t-1}+(1-\beta_{1})g_{t},\quad \hat{m}_{t}= \frac{m_{t}}{1-\beta_{1}^t} \tag{paper formulation} \\
m_{t} &= (1-\beta_{1})\sum_{i=0}^{t-1} \beta_{1}^{i}g_{t-1}+\beta_{1}^{t}m_{0} \tag{expanded form} \\
\hat{m}_{t} &= \frac{m_{t}}{1-\beta_{1}^t}
\end{align}
$$Where:
* $g_{t} = \Delta J(w_{t})$ is the gradient at step $t$
* $m_{t-1}$ is the EMO of the gradient **up to** step $t-1$
* $\beta_{1} \in [0,1)$ controls the decay rate of the EMA
	* Larger values emphasise older gradient values

**Second moment (uncentered variance)**:
$$
\begin{align}
v_{t}&=\beta_{2}v_{t-1}+(1-\beta_{2})g_{t}^2 \tag{paper formulation} \\
v_{t}&=(1-\beta_{2}) \sum_{i=1}^{t-1}\beta_{2}^i g_{t-i}^2v_{0} \tag{expanded form} \\
\hat{v}_{t} &= \frac{v_{t}}{1-\beta_{2}^t} \tag{final update}
\end{align}
$$Where:
* $g_{t}^2$ is the element-wise squared gradient
* $v_{t-1}$ is the EMA of the squared gradient **up to** step $t-1$
* $\beta_{2} \in [0,1)$ controls the decay rate of the EMA

## Adam as a [[Gradient Preconditioning|Preconditioner]]
Adam can be understood as a preconditioner with an update step written as:
$$
w_{t+1} = w_{t} - \eta_{t}P_{t}^{-1}\hat{m_{t}}
$$Where the preconditioning matrix $P$ is defined as:
$$
P_{t} = \text{diag}(\sqrt{ \hat{v}_{t,1}+\epsilon, \hat{v}_{t,2}+\epsilon,\dots, \hat{v}_{t,d} + \epsilon})
$$