*Sign descent* is an optimisation algorithm which only uses the sign of each component of the gradient, not the magnitude:
$$
w_{t+1}=w_{t}-\eta \cdot \text{sign}(\nabla f(w_{t}))
$$Where:
* $\text{sign}(x)$ returns $1$ if $x>0$, $-1$ if $x<0$, and $0$ if $x=0$.
* $\eta$ is the learning rate.
* $\nabla f(w_{t})$ is the gradient of all parameters $w$ at time step $t$.
