# Self-information
The information gained from observing a **specific** event $x \in X$. For an event $x$ with probability $p(x)$, the information content $I(x)$ is: 
$$
I(x) = -\log(p(x))
$$
Less probable events carry more information as they are more surprising.

# Entropy
The expected (average) gained from observing a random variable $X$, considering all possible outcomes $x \in X$ weighted by their probabilities.
## Shannon Entropy
For a random variable $X$ with a [[PMF]] $p(x)$, the Shannon entropy $H(X)$ is:
$$
H(X) = -log \sum\limits_{x}p(x)\log(p(x))
$$**Qualities:**
* Scale-invariant - $H(x) \geq 0$ 
## Differential Entropy
For a random variable $X$ with a [[PDF]] $p(x)$, the differential entropy $H(X)$ is:
$$
H(x) = -\int p(x)\log(p(x))dx
$$**Qualities:**
* Not scale-invariant - Can cause $H(x)$ to be negative
	* I.e., multiplying $x$ by a constant changes $H(x)$

**Selecting a logarithmic base:**
* $\log_{2}$ for bits, for binary systems
* $\log_e$ for *nats*, natural units of information
