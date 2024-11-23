Recall that differential equations represent dynamic systems. Consider a function $f(t)$ (or some data) and its derivative:
$$
\frac{df}{dt} = \lim_{\Delta t \rightarrow 0} \frac{f(t+\Delta t)-f(t)}{\Delta t}
$$
With the *finite difference* method, we instead approximate this by not taking the limit, and approximating the derivative as:
$$
\frac{df}{dt} \approx \frac{f(t+\Delta t)-f(t)}{\Delta t}
$$
## Estimating Approximation Error
## Particle Example
Now, consider a differential equation where the rate of change of $x$ w.r.t $t$ is given by $f(x(t))$. In this case, $x$ is a function of time $t$. The differential equation tells us how $x$ changes over $t$.
$$
\frac{dx}{dt}=f(x(t))
$$This shows that the rate of change of $x$ w.r.t time $t$ depends on the current value of $x(t)$, not directly on $t$. For example, if $x$ represents position, $f(x(t))$ describes how velocity changes based on the position at time $t$, not on time itself.`

This may be approximated by the finite difference method which uses a small timestep $\Delta t$:
$$
\implies \frac{x(t +\Delta t) -x(t)}{\Delta t} \approx f(x(t))
$$We now rewrite $x$ explicitly as a function of $t$: $x(t)$ 
We have replaced $f(x)$ with $f(t)$ as we are now evaluating the function at a specific time $t$. We are no longer concerned with the behaviour of $f$ at an arbitrary time $x$.