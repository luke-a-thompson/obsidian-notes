Similar to [[Linear Regression]], but we treat model weights as random variables, and quantify model uncertainty in the weights via probability distributions.

**Key difference vs linear regression:**
* Linear regression considers a single deterministic function $f(x) = w^{T}\phi(x)$ mapping $x$ to $y$.
* Bayesian linear regression assumes the weights $w$ follow a distribution, so there are many possible weights. **Hence, as each function has different weights, there is a distribution of possible functions, each with a different set of weights.**

Given a linear model, where $f(x)$ is the prediction, $w$ is the weight vector, and $\phi(x)$ is the input features:
$$
f(x) = w^{T}\phi(x)
$$
The observed data, $y$ is the output of a function plus noise $\epsilon \sim \mathcal{N}(x, \sigma^2)$:
$$
y = f(x) + \epsilon
$$

## Key Probability $Pr(\cdot)$ Distributions
### Prior
**We have a (usually Gaussian) prior distribution over the weights $w$**, before seeing data:
$$
Pr(w) \sim \mathcal{N}(\mu_{w, \Sigma_w})
$$
### Likelihood Distribution
**Likelihood of observing the set of outputs, $Y$, given the set of inputs $X$ and weights $w$:**
$$
Pr(Y|w,X) \sim \mathcal{N}(Xw, \sigma^{2})
$$
This is the joint likelihood of seeing $Y$ given all inputs $X$ and weights $w$. It is the product of the individual likelihoods for each datapoint:
$$
Pr(Y|w, X) = \prod\limits_{i=1}^{N}\mathcal{N}(y_{i}|w^{T}\phi(x_{i}, \sigma^{2}))
$$
Where:
${N}(y_{i}|w^{T}\phi(x_{i}), \sigma^{2}$ is the probability of observing $y_i$ given some weights and a transformed input $x_i$.

### Posterior Distribution
**Our updated belief about the weights is calculated using Bayes' theorem:**
$$
Pr(w|X,Y) = \frac{Pr(Y|w,X)Pr(w)}{Pr(Y|X)}
$$

## Function Space View
We consider a distribution over the possuble functions mapping $x$ to $y$. This is because the prior over parameters $w$ induces a prior over functions $f(x)$. As $w$ is Gaussian, $f(x)$ is as well.
