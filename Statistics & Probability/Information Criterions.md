## Akaike Information Criterion (AIC)
The AIC measures balances model fit with complexity to prevent overfitting. Generally **best for prediction**.

**Formula:**
$$
AIC = 2k - 2\log(\hat{L})
$$
Where:
* $k$ is the number of parameters
* $\hat{L}$ is the likelihood of the model given the data
	* I.e., the likelihood function, the probability of observing the data given a set of parameters of the model
	* For a set of datapoints $x$ and model parameters $\theta$, the likelihood is $p(x|\theta)$
	* "Given the data we observed, what parameters would make our model most likely to spit this data out"
	* But if we maximised this alone we'd be insanely overfit, hence, we need the AIC

## Bayesian Information Criterion
The BIC is similar to the AIC, but tends to **put greater penalties on large models**. Generally **best for finding the true model**.

**Formula:**
$$
BIC = k \log(n) - 2 \log(\hat{L})
$$
Where:
* $k$ is the number of parameters
* $n$ is the number of datapoints (sample size)
* $\hat{L}$ is the maximised value of the likelihood function

Why is it different?
* Based on the [[Bayes Factor]]
* Tries to identify the most likely model given the data, assuming one of the models is true
