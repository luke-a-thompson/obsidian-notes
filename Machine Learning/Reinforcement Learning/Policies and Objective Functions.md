A conventional RL objective function $J$ may be denoted:
$$
J(\theta) := \mathbb{E}_{\tau \sim p(\tau | P)} [R(\tau, (X,y))]
$$
Where:
* $\theta$ is the parameters of the policy
* $\tau$ is a trajectory of states and actions sampled from $p(\tau | \theta)$
* $R(\tau, (X,y))$ is the *reward* associated with a trajectory $\tau$ given input data $(X,y)$

## Policy Gradients
* A risk-seeking policy gradient algorithm favours high-risk high-reward actions
	* In practice, optimises for trajectories with higher variance and rewards*
