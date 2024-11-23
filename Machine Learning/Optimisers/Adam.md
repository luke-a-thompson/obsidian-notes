*Adam* is a (diagonally) [[Gradient Preconditioning|preconditioned]] [[Stochastic Gradient Descent|gradient descent]] algorithm incorporating adaptive per-parameter scaling and momentum accumulation. It is written as:
$$
\begin{align} \\
g_{t} &= \Delta J(w_{t}) + \lambda w_{t} \\
m_{t} &= \beta_{1}m_{t-1}+(1-\beta_{1})g_{t},& \hat{m}_{t}= \frac{m_{t}}{1-\beta_{1}^t} \tag{first moment} \\ \\
v_{t}&=\beta_{2}v_{t-1}+(1-\beta_{2})g_{t}^2,& \hat{v}_{t} = \frac{v_{t}}{1-\beta_{2}^t} \tag{second moment} \\
w_{t+1}&=w_t- \eta \frac{\hat{m}_{t}}{\sqrt{ \hat{v}_{t} }+\epsilon} \tag{update}
\end{align}
$$Where:
* $J(w_{t})$ is the derivative of the loss function w.r.t some weight
* $\lambda w_{t}$ represents an optional $\ell_{2}$ weight decay term with a decay coefficient $\lambda$
* $\hat{m}_{t}, \hat{v}_{t}$ are the first and second moments of the gradient at time $t$
* $w_{t}$ is a weight at some time $t$
* $\eta$ is the learning rate
* $\epsilon$ is a small constant preventing division by $0$

## Moment Estimation
Adam maintains two moment estimates for the gradients:
**First moment (mean)**:
$$\begin{align}
m_{t} &= \beta_{1}m_{t-1}+(1-\beta_{1})g_{t} \tag{paper formulation} \\
m_{t} &= (1-\beta_{1})\sum_{i=0}^{t-1} \beta_{1}^{i}g_{t-1}+\beta_{1}^{t}m_{0} \tag{expanded form} \\
\hat{m}_{t} &= \frac{m_{t}}{1-\beta_{1}^t} \tag{final update}
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
P_{t} = \text{diag}(\sqrt{\hat{v}_{t,1}} + \epsilon, \sqrt{\hat{v}_{t,2}} + \epsilon, \dots, \sqrt{\hat{v}_{t,d}} + \epsilon)

$$Where:
* Each parameter $w_{i}$ is scaled by $\sqrt{ \hat{v}_{t,i} }$ reflecting the variance of its gradient over time
* Both $\hat{m}_{t}, P_{t}$ depend on time $t$
* $\epsilon$ avoids divide by $0$ when $v_{t}$ is small

We can then reformulate the update as minimising a quadratic approximation of the objective function $J(w)$ under a preconditioned norm:
$$
\min_{\Delta w} \left[g_{t}^T \Delta w + \frac{1}{2\eta_{t}}\|\Delta w\|_{P_{t}}^{2} \right]
$$Yielding the update:
$$\begin{align}
\Delta w&=-\eta P^{-1}g \tag{with explicit matrix computation} \\
\Delta w&=-\eta (P^{-1}g + \lambda w) \tag{with Euclidian weight decay} \\
\end{align}
$$In practice, the update is done in a **matrix-free fashion**:
$$
w_{t+1,i} = w_{t,i}- \frac{\eta_{t}\hat{m}_{t,i}}{\sqrt{ \hat{v}_{t,i} }+\epsilon} \tag{actual matrix-free implementation}
$$
Where:
* $g_{t} = \hat{m}_{t}$ is the bias-corrected first moment (directional component)
* $w_{t,i}$ is some parameter $i$ at time $t$
* $\|\Delta w\|_{P_{t}}^2= \Delta w^TP_{t}\Delta w$ penalises the size of the update based on the preconditioning matrix $P$
	* If $P$ has large $\lambda$ in certain directions, $P^{-1}$ shrinks those updates
	* **This is equivalent to a quadratic penalty (hence the norm) on $\Delta w$ preventing updates from being excessively large**
